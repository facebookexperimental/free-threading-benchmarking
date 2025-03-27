# Results vs. base

- fork: Yhg1s
- ref: avoid_list_critsect
- machine: darwin-arm64
- commit hash: e69e45f
- commit date: 2025-03-27
- overall geometric mean: 1.001x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                   | 112 ms: 1.02x faster                                                   |
| docutils       | 974 ms                                                                   | 966 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators                 | 170 ms                                                                   | 168 ms: 1.01x faster                                                   |
| async_tree_none                  | 99.6 ms                                                                  | 98.6 ms: 1.01x faster                                                  |
| async_tree_eager_io              | 198 ms                                                                   | 196 ms: 1.01x faster                                                   |
| async_tree_eager                 | 46.5 ms                                                                  | 46.1 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 230 ms                                                                   | 228 ms: 1.01x faster                                                   |
| async_tree_eager_io_tg           | 186 ms                                                                   | 184 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed          | 240 ms                                                                   | 238 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 217 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 220 ms                                                                   | 219 ms: 1.01x faster                                                   |
| async_tree_eager_tg              | 74.4 ms                                                                  | 73.9 ms: 1.01x faster                                                  |
| async_tree_eager_memoization     | 108 ms                                                                   | 108 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                                   | 189 ms: 1.01x faster                                                   |
| async_tree_memoization           | 129 ms                                                                   | 128 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 109 ms                                                                   | 109 ms: 1.00x faster                                                   |
| async_tree_memoization_tg        | 121 ms                                                                   | 120 ms: 1.00x faster                                                   |
| async_tree_none_tg               | 82.7 ms                                                                  | 82.4 ms: 1.00x faster                                                  |
| async_tree_io                    | 205 ms                                                                   | 204 ms: 1.00x faster                                                   |
| async_tree_io_tg                 | 189 ms                                                                   | 189 ms: 1.00x faster                                                   |
| coroutines                       | 9.08 ms                                                                  | 9.21 ms: 1.01x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 61.5 ms                                                                  | 58.8 ms: 1.04x faster                                                  |
| float          | 29.0 ms                                                                  | 28.8 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 48.9 ms                                                                  | 49.0 ms: 1.00x slower                                                  |
| regex_dna      | 102 ms                                                                   | 103 ms: 1.01x slower                                                   |
| regex_v8       | 10.1 ms                                                                  | 10.1 ms: 1.01x slower                                                  |
| regex_effbot   | 1.50 ms                                                                  | 1.51 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|---------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_generate  | 34.4 ms                                                                  | 33.8 ms: 1.02x faster                                                  |
| xml_etree_process   | 24.9 ms                                                                  | 24.9 ms: 1.00x slower                                                  |
| json_dumps          | 5.04 ms                                                                  | 5.08 ms: 1.01x slower                                                  |
| xml_etree_iterparse | 34.7 ms                                                                  | 37.6 ms: 1.08x slower                                                  |
| xml_etree_parse     | 55.7 ms                                                                  | 60.7 ms: 1.09x slower                                                  |
| Geometric mean      | (ref)                                                                    | 1.02x slower                                                           |

Benchmark hidden because not significant (4): json_loads, unpickle_pure_python, tomli_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.16 ms                                                                  | 9.15 ms: 1.00x faster                                                  |
| python_startup_no_site | 7.25 ms                                                                  | 7.24 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 20.8 ms                                                                  | 21.0 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                           |

Benchmark hidden because not significant (3): django_template, mako, genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody                            | 61.5 ms                                                                  | 58.8 ms: 1.04x faster                                                  |
| xml_etree_generate               | 34.4 ms                                                                  | 33.8 ms: 1.02x faster                                                  |
| fannkuch                         | 189 ms                                                                   | 186 ms: 1.02x faster                                                   |
| telco                            | 3.28 ms                                                                  | 3.23 ms: 1.02x faster                                                  |
| many_optionals                   | 233 us                                                                   | 230 us: 1.02x faster                                                   |
| scimark_monte_carlo              | 33.8 ms                                                                  | 33.3 ms: 1.02x faster                                                  |
| 2to3                             | 114 ms                                                                   | 112 ms: 1.02x faster                                                   |
| subparsers                       | 8.39 ms                                                                  | 8.29 ms: 1.01x faster                                                  |
| async_generators                 | 170 ms                                                                   | 168 ms: 1.01x faster                                                   |
| async_tree_none                  | 99.6 ms                                                                  | 98.6 ms: 1.01x faster                                                  |
| async_tree_eager_io              | 198 ms                                                                   | 196 ms: 1.01x faster                                                   |
| deepcopy_reduce                  | 1.12 us                                                                  | 1.11 us: 1.01x faster                                                  |
| scimark_fft                      | 140 ms                                                                   | 139 ms: 1.01x faster                                                   |
| bench_mp_pool                    | 39.6 ms                                                                  | 39.2 ms: 1.01x faster                                                  |
| async_tree_eager                 | 46.5 ms                                                                  | 46.1 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 230 ms                                                                   | 228 ms: 1.01x faster                                                   |
| async_tree_eager_io_tg           | 186 ms                                                                   | 184 ms: 1.01x faster                                                   |
| go                               | 58.1 ms                                                                  | 57.6 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed          | 240 ms                                                                   | 238 ms: 1.01x faster                                                   |
| docutils                         | 974 ms                                                                   | 966 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 217 ms: 1.01x faster                                                   |
| dulwich_log                      | 17.9 ms                                                                  | 17.7 ms: 1.01x faster                                                  |
| generators                       | 14.0 ms                                                                  | 13.9 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed_tg | 220 ms                                                                   | 219 ms: 1.01x faster                                                   |
| async_tree_eager_tg              | 74.4 ms                                                                  | 73.9 ms: 1.01x faster                                                  |
| float                            | 29.0 ms                                                                  | 28.8 ms: 1.01x faster                                                  |
| async_tree_eager_memoization     | 108 ms                                                                   | 108 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                                   | 189 ms: 1.01x faster                                                   |
| deepcopy                         | 107 us                                                                   | 107 us: 1.01x faster                                                   |
| sqlalchemy_declarative           | 47.5 ms                                                                  | 47.3 ms: 1.01x faster                                                  |
| async_tree_memoization           | 129 ms                                                                   | 128 ms: 1.01x faster                                                   |
| hexiom                           | 2.92 ms                                                                  | 2.91 ms: 1.00x faster                                                  |
| sqlalchemy_imperative            | 5.37 ms                                                                  | 5.35 ms: 1.00x faster                                                  |
| sqlglot_v2_parse                 | 562 us                                                                   | 559 us: 1.00x faster                                                   |
| k_core                           | 1.01 sec                                                                 | 1.00 sec: 1.00x faster                                                 |
| async_tree_eager_memoization_tg  | 109 ms                                                                   | 109 ms: 1.00x faster                                                   |
| sympy_sum                        | 57.1 ms                                                                  | 56.9 ms: 1.00x faster                                                  |
| async_tree_memoization_tg        | 121 ms                                                                   | 120 ms: 1.00x faster                                                   |
| async_tree_none_tg               | 82.7 ms                                                                  | 82.4 ms: 1.00x faster                                                  |
| spectral_norm                    | 49.8 ms                                                                  | 49.7 ms: 1.00x faster                                                  |
| async_tree_io                    | 205 ms                                                                   | 204 ms: 1.00x faster                                                   |
| async_tree_io_tg                 | 189 ms                                                                   | 189 ms: 1.00x faster                                                   |
| bpe_tokeniser                    | 1.93 sec                                                                 | 1.92 sec: 1.00x faster                                                 |
| python_startup                   | 9.16 ms                                                                  | 9.15 ms: 1.00x faster                                                  |
| python_startup_no_site           | 7.25 ms                                                                  | 7.24 ms: 1.00x faster                                                  |
| regex_compile                    | 48.9 ms                                                                  | 49.0 ms: 1.00x slower                                                  |
| pprint_pformat                   | 685 ms                                                                   | 686 ms: 1.00x slower                                                   |
| xml_etree_process                | 24.9 ms                                                                  | 24.9 ms: 1.00x slower                                                  |
| richards                         | 21.8 ms                                                                  | 21.9 ms: 1.00x slower                                                  |
| raytrace                         | 128 ms                                                                   | 129 ms: 1.00x slower                                                   |
| logging_simple                   | 2.36 us                                                                  | 2.38 us: 1.01x slower                                                  |
| regex_dna                        | 102 ms                                                                   | 103 ms: 1.01x slower                                                   |
| pathlib                          | 11.1 ms                                                                  | 11.1 ms: 1.01x slower                                                  |
| regex_v8                         | 10.1 ms                                                                  | 10.1 ms: 1.01x slower                                                  |
| richards_super                   | 25.1 ms                                                                  | 25.3 ms: 1.01x slower                                                  |
| coverage                         | 38.3 ms                                                                  | 38.5 ms: 1.01x slower                                                  |
| genshi_xml                       | 20.8 ms                                                                  | 21.0 ms: 1.01x slower                                                  |
| regex_effbot                     | 1.50 ms                                                                  | 1.51 ms: 1.01x slower                                                  |
| meteor_contest                   | 53.1 ms                                                                  | 53.5 ms: 1.01x slower                                                  |
| mdp                              | 1.10 sec                                                                 | 1.11 sec: 1.01x slower                                                 |
| scimark_lu                       | 50.6 ms                                                                  | 51.0 ms: 1.01x slower                                                  |
| thrift                           | 307 us                                                                   | 310 us: 1.01x slower                                                   |
| json_dumps                       | 5.04 ms                                                                  | 5.08 ms: 1.01x slower                                                  |
| create_gc_cycles                 | 457 us                                                                   | 463 us: 1.01x slower                                                   |
| coroutines                       | 9.08 ms                                                                  | 9.21 ms: 1.01x slower                                                  |
| pyflate                          | 194 ms                                                                   | 198 ms: 1.02x slower                                                   |
| logging_silent                   | 41.5 ns                                                                  | 43.4 ns: 1.05x slower                                                  |
| xml_etree_iterparse              | 34.7 ms                                                                  | 37.6 ms: 1.08x slower                                                  |
| xml_etree_parse                  | 55.7 ms                                                                  | 60.7 ms: 1.09x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (35): pylint, bench_thread_pool, scimark_sparse_mat_mult, json_loads, sqlglot_v2_transpile, unpickle_pure_python, sqlglot_v2_optimize, tomli_loads, pidigits, crypto_pyaes, sphinx, django_template, sqlglot_v2_normalize, chaos, comprehensions, sympy_integrate, connected_components, pycparser, sqlite_synth, sympy_str, mako, deepcopy_memo, sympy_expand, pprint_safe_repr, nqueens, genshi_text, scimark_sor, typing_runtime_protocols, pickle_pure_python, logging_format, shortest_path, deltablue, json, html5lib, gc_traversal

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x