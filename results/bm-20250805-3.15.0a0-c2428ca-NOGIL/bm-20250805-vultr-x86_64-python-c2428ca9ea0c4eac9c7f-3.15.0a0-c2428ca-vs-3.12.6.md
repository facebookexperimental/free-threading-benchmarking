# Results vs. 3.12.6

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: linux-x86_64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.028x slower
- HPT reliability: 94.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.71 sec: 1.03x slower                                                |
| html5lib       | 63.6 ms                                                | 68.3 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 202 ms: 1.09x slower                                                  |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.01x slower                                                 |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.06x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 346 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.52 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.1 ms: 1.14x slower                                                 |
| django_template | 34.7 ms                                                | 40.5 ms: 1.17x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 16.0 ms: 1.46x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.94 ms: 1.79x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 300 us: 1.17x faster                                                  |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 35.2 us: 1.14x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.7 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| generators                 | 32.2 ms                                                | 30.5 ms: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.04x faster                                                  |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.10 us: 1.01x slower                                                 |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.01x slower                                                 |
| raytrace                   | 299 ms                                                 | 304 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.71 sec: 1.03x slower                                                |
| pyflate                    | 448 ms                                                 | 461 ms: 1.03x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.49 ms: 1.05x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.99 us: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.68 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 797 ms: 1.07x slower                                                  |
| html5lib                   | 63.6 ms                                                | 68.3 ms: 1.07x slower                                                 |
| logging_format             | 7.35 us                                                | 7.89 us: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                 |
| scimark_fft                | 342 ms                                                 | 369 ms: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.08x slower                                                |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.5 ms: 1.09x slower                                                 |
| pidigits                   | 184 ms                                                 | 202 ms: 1.09x slower                                                  |
| richards                   | 45.9 ms                                                | 51.3 ms: 1.12x slower                                                 |
| thrift                     | 791 us                                                 | 888 us: 1.12x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.1 ms: 1.12x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 346 us: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 527 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.9 ms: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.1 ms: 1.14x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.1 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 187 us: 1.15x slower                                                  |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| django_template            | 34.7 ms                                                | 40.5 ms: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                 |
| fannkuch                   | 372 ms                                                 | 452 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.77 ms: 1.31x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.52 ms: 1.33x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.52 ms: 1.39x slower                                                 |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.46x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.08x slower                                                 |
| telco                      | 6.53 ms                                                | 177 ms: 27.05x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.028x slower

# HPT report

- Reliability score: 94.80% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x