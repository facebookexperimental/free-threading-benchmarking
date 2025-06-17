# Results vs. 3.12.6

- fork: python
- ref: fba5dded6df3c2b19435
- machine: linux-x86_64
- commit hash: fba5dde
- commit date: 2025-06-17
- overall geometric mean: 1.014x faster
- HPT reliability: 84.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| html5lib       | 63.6 ms                                                | 66.2 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 526 ms: 2.11x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.98x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 288 ms: 1.94x faster                                                  |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.5 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                  |
| nbody          | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                |
| unpickle_pure_python | 221 us                                                 | 230 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 94.9 ms: 1.11x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.9 us: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 526 ms: 2.11x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.98x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 288 ms: 1.94x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.81x faster                                                 |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                  |
| deepcopy                   | 352 us                                                 | 285 us: 1.24x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.4 us: 1.17x faster                                                 |
| float                      | 80.8 ms                                                | 69.5 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| generators                 | 32.2 ms                                                | 30.1 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.99 us: 1.03x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                  |
| chaos                      | 62.8 ms                                                | 62.0 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.38 ms: 1.03x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.2 ms: 1.04x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 230 us: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.60 ms: 1.05x slower                                                 |
| scimark_fft                | 342 ms                                                 | 362 ms: 1.06x slower                                                  |
| pyflate                    | 448 ms                                                 | 475 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                 |
| nqueens                    | 80.1 ms                                                | 85.6 ms: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 75.8 ms: 1.11x slower                                                 |
| thrift                     | 791 us                                                 | 882 us: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 94.9 ms: 1.11x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.4 ms: 1.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                  |
| richards                   | 45.9 ms                                                | 51.6 ms: 1.12x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.54 us: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 188 us: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.8 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                 |
| logging_format             | 7.35 us                                                | 8.52 us: 1.16x slower                                                 |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 874 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.80 sec: 1.18x slower                                                |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.9 us: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.58 ms: 1.27x slower                                                 |
| telco                      | 6.53 ms                                                | 8.43 ms: 1.29x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.47 ms: 1.35x slower                                                 |
| nbody                      | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.10 ms: 3.30x slower                                                 |
| logging_silent             | 109 ns                                                 | 526 ns: 4.82x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250617-3.15.0a0-fba5dde-NOGIL/bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 84.76% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x