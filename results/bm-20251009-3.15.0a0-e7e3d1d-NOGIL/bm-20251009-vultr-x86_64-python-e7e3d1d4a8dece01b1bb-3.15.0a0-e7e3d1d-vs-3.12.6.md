# Results vs. 3.12.6

- fork: python
- ref: e7e3d1d4a8dece01b1bb
- machine: linux-x86_64
- commit hash: e7e3d1d
- commit date: 2025-10-09
- overall geometric mean: 1.016x slower
- HPT reliability: 78.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| html5lib       | 63.6 ms                                                | 68.4 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 515 ms: 2.15x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 280 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 546 ms: 1.98x faster                                                  |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 466 ms: 1.55x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                 |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                  |
| nbody          | 89.3 ms                                                | 119 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.7 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.03 sec: 1.04x faster                                                |
| unpickle_pure_python | 221 us                                                 | 234 us: 1.06x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 342 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.4 ms: 1.12x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| django_template | 34.7 ms                                                | 41.4 ms: 1.19x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 515 ms: 2.15x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 280 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 546 ms: 1.98x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.95 ms: 1.77x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 466 ms: 1.55x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.8 us: 1.31x faster                                                 |
| deepcopy                   | 352 us                                                 | 281 us: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                 |
| float                      | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 86.7 ms: 1.11x faster                                                 |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| generators                 | 32.2 ms                                                | 30.1 ms: 1.07x faster                                                 |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.03 sec: 1.04x faster                                                |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.96 us: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| raytrace                   | 299 ms                                                 | 297 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.4 ms: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| scimark_fft                | 342 ms                                                 | 347 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.80 us: 1.03x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.45 ms: 1.05x slower                                                 |
| pyflate                    | 448 ms                                                 | 471 ms: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| logging_format             | 7.35 us                                                | 7.75 us: 1.06x slower                                                 |
| sympy_str                  | 292 ms                                                 | 308 ms: 1.06x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 787 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 234 us: 1.06x slower                                                  |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.07x slower                                                |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                 |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                  |
| html5lib                   | 63.6 ms                                                | 68.4 ms: 1.08x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.76 ms: 1.09x slower                                                 |
| nqueens                    | 80.1 ms                                                | 88.1 ms: 1.10x slower                                                 |
| sympy_expand               | 468 ms                                                 | 519 ms: 1.11x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 342 us: 1.11x slower                                                  |
| thrift                     | 791 us                                                 | 887 us: 1.12x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.1 ms: 1.12x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 56.4 ms: 1.12x slower                                                 |
| richards                   | 45.9 ms                                                | 51.7 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 78.3 ms: 1.14x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.6 ms: 1.15x slower                                                 |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.16x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| django_template            | 34.7 ms                                                | 41.4 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.31 ms: 1.21x slower                                                 |
| fannkuch                   | 372 ms                                                 | 456 ms: 1.22x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 119 ms: 1.34x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 15.0 ms: 1.39x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.53 ms: 1.40x slower                                                 |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.05 ms: 3.24x slower                                                 |
| telco                      | 6.53 ms                                                | 177 ms: 27.08x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 78.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x