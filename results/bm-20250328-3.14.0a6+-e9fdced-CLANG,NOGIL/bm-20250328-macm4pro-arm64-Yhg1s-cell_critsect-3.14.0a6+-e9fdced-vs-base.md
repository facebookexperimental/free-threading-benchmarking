# Results vs. base

- fork: Yhg1s
- ref: cell_critsect
- machine: darwin-arm64
- commit hash: e9fdced
- commit date: 2025-03-28
- overall geometric mean: 1.003x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 114 ms                                                                   | 112 ms: 1.02x faster                                             |
| docutils       | 974 ms                                                                   | 960 ms: 1.02x faster                                             |
| sphinx         | 400 ms                                                                   | 397 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                     |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_generators                 | 170 ms                                                                   | 166 ms: 1.03x faster                                             |
| async_tree_cpu_io_mixed          | 240 ms                                                                   | 236 ms: 1.02x faster                                             |
| async_tree_none                  | 99.6 ms                                                                  | 98.1 ms: 1.02x faster                                            |
| asyncio_websockets               | 190 ms                                                                   | 188 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed_tg       | 230 ms                                                                   | 226 ms: 1.01x faster                                             |
| async_tree_eager_io              | 198 ms                                                                   | 195 ms: 1.01x faster                                             |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 216 ms: 1.01x faster                                             |
| async_tree_eager_io_tg           | 186 ms                                                                   | 183 ms: 1.01x faster                                             |
| async_tree_eager_cpu_io_mixed_tg | 220 ms                                                                   | 218 ms: 1.01x faster                                             |
| async_tree_eager_tg              | 74.4 ms                                                                  | 73.7 ms: 1.01x faster                                            |
| async_tree_memoization           | 129 ms                                                                   | 128 ms: 1.01x faster                                             |
| async_tree_eager_memoization     | 108 ms                                                                   | 108 ms: 1.01x faster                                             |
| async_tree_eager                 | 46.5 ms                                                                  | 46.2 ms: 1.01x faster                                            |
| async_tree_io                    | 205 ms                                                                   | 203 ms: 1.01x faster                                             |
| async_tree_io_tg                 | 189 ms                                                                   | 188 ms: 1.01x faster                                             |
| async_tree_none_tg               | 82.7 ms                                                                  | 82.2 ms: 1.01x faster                                            |
| async_tree_memoization_tg        | 121 ms                                                                   | 120 ms: 1.00x faster                                             |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                     |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 61.5 ms                                                                  | 59.6 ms: 1.03x faster                                            |
| pidigits       | 163 ms                                                                   | 160 ms: 1.02x faster                                             |
| float          | 29.0 ms                                                                  | 28.8 ms: 1.01x faster                                            |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_v8       | 10.1 ms                                                                  | 9.92 ms: 1.02x faster                                            |
| regex_dna      | 102 ms                                                                   | 100 ms: 1.02x faster                                             |
| regex_effbot   | 1.50 ms                                                                  | 1.48 ms: 1.01x faster                                            |
| regex_compile  | 48.9 ms                                                                  | 49.1 ms: 1.00x slower                                            |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|---------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_dumps          | 5.04 ms                                                                  | 4.98 ms: 1.01x faster                                            |
| json_loads          | 11.7 us                                                                  | 11.6 us: 1.01x faster                                            |
| xml_etree_iterparse | 34.7 ms                                                                  | 34.8 ms: 1.00x slower                                            |
| xml_etree_parse     | 55.7 ms                                                                  | 55.9 ms: 1.00x slower                                            |
| xml_etree_process   | 24.9 ms                                                                  | 25.0 ms: 1.01x slower                                            |
| xml_etree_generate  | 34.4 ms                                                                  | 34.6 ms: 1.01x slower                                            |
| pickle_pure_python  | 138 us                                                                   | 140 us: 1.01x slower                                             |
| Geometric mean      | (ref)                                                                    | 1.00x slower                                                     |

Benchmark hidden because not significant (2): unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 9.16 ms                                                                  | 9.13 ms: 1.00x faster                                            |
| python_startup_no_site | 7.25 ms                                                                  | 7.23 ms: 1.00x faster                                            |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| django_template | 15.1 ms                                                                  | 15.2 ms: 1.01x slower                                            |
| Geometric mean  | (ref)                                                                    | 1.00x slower                                                     |

Benchmark hidden because not significant (3): genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody                            | 61.5 ms                                                                  | 59.6 ms: 1.03x faster                                            |
| async_generators                 | 170 ms                                                                   | 166 ms: 1.03x faster                                             |
| many_optionals                   | 233 us                                                                   | 228 us: 1.02x faster                                             |
| 2to3                             | 114 ms                                                                   | 112 ms: 1.02x faster                                             |
| gc_traversal                     | 758 us                                                                   | 745 us: 1.02x faster                                             |
| async_tree_cpu_io_mixed          | 240 ms                                                                   | 236 ms: 1.02x faster                                             |
| pidigits                         | 163 ms                                                                   | 160 ms: 1.02x faster                                             |
| regex_v8                         | 10.1 ms                                                                  | 9.92 ms: 1.02x faster                                            |
| async_tree_none                  | 99.6 ms                                                                  | 98.1 ms: 1.02x faster                                            |
| docutils                         | 974 ms                                                                   | 960 ms: 1.02x faster                                             |
| regex_dna                        | 102 ms                                                                   | 100 ms: 1.02x faster                                             |
| generators                       | 14.0 ms                                                                  | 13.8 ms: 1.02x faster                                            |
| asyncio_websockets               | 190 ms                                                                   | 188 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed_tg       | 230 ms                                                                   | 226 ms: 1.01x faster                                             |
| async_tree_eager_io              | 198 ms                                                                   | 195 ms: 1.01x faster                                             |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 216 ms: 1.01x faster                                             |
| regex_effbot                     | 1.50 ms                                                                  | 1.48 ms: 1.01x faster                                            |
| subparsers                       | 8.39 ms                                                                  | 8.28 ms: 1.01x faster                                            |
| bench_mp_pool                    | 39.6 ms                                                                  | 39.1 ms: 1.01x faster                                            |
| async_tree_eager_io_tg           | 186 ms                                                                   | 183 ms: 1.01x faster                                             |
| create_gc_cycles                 | 457 us                                                                   | 451 us: 1.01x faster                                             |
| async_tree_eager_cpu_io_mixed_tg | 220 ms                                                                   | 218 ms: 1.01x faster                                             |
| json_dumps                       | 5.04 ms                                                                  | 4.98 ms: 1.01x faster                                            |
| json_loads                       | 11.7 us                                                                  | 11.6 us: 1.01x faster                                            |
| async_tree_eager_tg              | 74.4 ms                                                                  | 73.7 ms: 1.01x faster                                            |
| async_tree_memoization           | 129 ms                                                                   | 128 ms: 1.01x faster                                             |
| sympy_integrate                  | 7.87 ms                                                                  | 7.80 ms: 1.01x faster                                            |
| crypto_pyaes                     | 39.7 ms                                                                  | 39.4 ms: 1.01x faster                                            |
| dulwich_log                      | 17.9 ms                                                                  | 17.7 ms: 1.01x faster                                            |
| sphinx                           | 400 ms                                                                   | 397 ms: 1.01x faster                                             |
| sqlalchemy_imperative            | 5.37 ms                                                                  | 5.33 ms: 1.01x faster                                            |
| async_tree_eager_memoization     | 108 ms                                                                   | 108 ms: 1.01x faster                                             |
| async_tree_eager                 | 46.5 ms                                                                  | 46.2 ms: 1.01x faster                                            |
| float                            | 29.0 ms                                                                  | 28.8 ms: 1.01x faster                                            |
| spectral_norm                    | 49.8 ms                                                                  | 49.5 ms: 1.01x faster                                            |
| sympy_sum                        | 57.1 ms                                                                  | 56.7 ms: 1.01x faster                                            |
| k_core                           | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                           |
| pycparser                        | 449 ms                                                                   | 446 ms: 1.01x faster                                             |
| sqlalchemy_declarative           | 47.5 ms                                                                  | 47.2 ms: 1.01x faster                                            |
| async_tree_io                    | 205 ms                                                                   | 203 ms: 1.01x faster                                             |
| async_tree_io_tg                 | 189 ms                                                                   | 188 ms: 1.01x faster                                             |
| async_tree_none_tg               | 82.7 ms                                                                  | 82.2 ms: 1.01x faster                                            |
| telco                            | 3.28 ms                                                                  | 3.26 ms: 1.01x faster                                            |
| sympy_str                        | 104 ms                                                                   | 104 ms: 1.00x faster                                             |
| async_tree_memoization_tg        | 121 ms                                                                   | 120 ms: 1.00x faster                                             |
| hexiom                           | 2.92 ms                                                                  | 2.91 ms: 1.00x faster                                            |
| bpe_tokeniser                    | 1.93 sec                                                                 | 1.92 sec: 1.00x faster                                           |
| python_startup                   | 9.16 ms                                                                  | 9.13 ms: 1.00x faster                                            |
| python_startup_no_site           | 7.25 ms                                                                  | 7.23 ms: 1.00x faster                                            |
| shortest_path                    | 237 ms                                                                   | 237 ms: 1.00x faster                                             |
| xml_etree_iterparse              | 34.7 ms                                                                  | 34.8 ms: 1.00x slower                                            |
| raytrace                         | 128 ms                                                                   | 129 ms: 1.00x slower                                             |
| xml_etree_parse                  | 55.7 ms                                                                  | 55.9 ms: 1.00x slower                                            |
| regex_compile                    | 48.9 ms                                                                  | 49.1 ms: 1.00x slower                                            |
| pyflate                          | 194 ms                                                                   | 195 ms: 1.00x slower                                             |
| pprint_safe_repr                 | 337 ms                                                                   | 339 ms: 1.00x slower                                             |
| pprint_pformat                   | 685 ms                                                                   | 688 ms: 1.00x slower                                             |
| deepcopy                         | 107 us                                                                   | 108 us: 1.00x slower                                             |
| scimark_monte_carlo              | 33.8 ms                                                                  | 34.0 ms: 1.01x slower                                            |
| chaos                            | 27.9 ms                                                                  | 28.1 ms: 1.01x slower                                            |
| xml_etree_process                | 24.9 ms                                                                  | 25.0 ms: 1.01x slower                                            |
| xml_etree_generate               | 34.4 ms                                                                  | 34.6 ms: 1.01x slower                                            |
| sympy_expand                     | 175 ms                                                                   | 176 ms: 1.01x slower                                             |
| deepcopy_memo                    | 13.2 us                                                                  | 13.3 us: 1.01x slower                                            |
| django_template                  | 15.1 ms                                                                  | 15.2 ms: 1.01x slower                                            |
| deltablue                        | 1.54 ms                                                                  | 1.55 ms: 1.01x slower                                            |
| scimark_lu                       | 50.6 ms                                                                  | 51.1 ms: 1.01x slower                                            |
| scimark_fft                      | 140 ms                                                                   | 142 ms: 1.01x slower                                             |
| go                               | 58.1 ms                                                                  | 58.7 ms: 1.01x slower                                            |
| pickle_pure_python               | 138 us                                                                   | 140 us: 1.01x slower                                             |
| coverage                         | 38.3 ms                                                                  | 38.8 ms: 1.01x slower                                            |
| thrift                           | 307 us                                                                   | 313 us: 1.02x slower                                             |
| richards                         | 21.8 ms                                                                  | 22.3 ms: 1.02x slower                                            |
| scimark_sor                      | 53.4 ms                                                                  | 54.5 ms: 1.02x slower                                            |
| richards_super                   | 25.1 ms                                                                  | 25.6 ms: 1.02x slower                                            |
| scimark_sparse_mat_mult          | 2.23 ms                                                                  | 2.28 ms: 1.03x slower                                            |
| logging_silent                   | 41.5 ns                                                                  | 43.0 ns: 1.04x slower                                            |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                     |

Benchmark hidden because not significant (27): pylint, bench_thread_pool, deepcopy_reduce, genshi_xml, logging_format, sqlglot_v2_parse, logging_simple, async_tree_eager_memoization_tg, html5lib, sqlglot_v2_optimize, sqlglot_v2_transpile, connected_components, json, unpickle_pure_python, fannkuch, sqlite_synth, pathlib, nqueens, mdp, meteor_contest, mako, sqlglot_v2_normalize, coroutines, comprehensions, genshi_text, tomli_loads, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x