# Results vs. base

- fork: Fidget-Spinner
- ref: loop_2000
- machine: darwin-arm64
- commit hash: cec96a9
- commit date: 2026-01-24
- overall geometric mean: 1.005x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 111 ms                                                                   | 109 ms: 1.03x faster                                                    |
| docutils       | 992 ms                                                                   | 983 ms: 1.01x faster                                                    |
| html5lib       | 19.2 ms                                                                  | 20.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators                 | 183 ms                                                                   | 179 ms: 1.03x faster                                                    |
| async_tree_eager_tg              | 77.4 ms                                                                  | 75.9 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 215 ms: 1.02x faster                                                    |
| async_tree_none                  | 96.4 ms                                                                  | 94.7 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed          | 245 ms                                                                   | 241 ms: 1.02x faster                                                    |
| async_tree_eager                 | 37.3 ms                                                                  | 36.7 ms: 1.02x faster                                                   |
| coroutines                       | 10.2 ms                                                                  | 10.1 ms: 1.02x faster                                                   |
| async_tree_io                    | 226 ms                                                                   | 222 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 251 ms                                                                   | 247 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 238 ms                                                                   | 235 ms: 1.01x faster                                                    |
| asyncio_websockets               | 186 ms                                                                   | 184 ms: 1.01x faster                                                    |
| async_tree_eager_memoization     | 105 ms                                                                   | 105 ms: 1.01x faster                                                    |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (7): async_tree_eager_io, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_eager_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 160 ms                                                                   | 159 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 40.8 ms                                                                  | 40.1 ms: 1.02x faster                                                   |
| regex_effbot   | 1.43 ms                                                                  | 1.45 ms: 1.01x slower                                                   |
| regex_dna      | 93.6 ms                                                                  | 95.8 ms: 1.02x slower                                                   |
| regex_v8       | 9.50 ms                                                                  | 9.83 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 113 us                                                                   | 111 us: 1.02x faster                                                    |
| xml_etree_process    | 22.1 ms                                                                  | 21.6 ms: 1.02x faster                                                   |
| xml_etree_generate   | 31.3 ms                                                                  | 30.8 ms: 1.02x faster                                                   |
| json_dumps           | 3.63 ms                                                                  | 3.60 ms: 1.01x faster                                                   |
| unpickle_pure_python | 74.0 us                                                                  | 75.4 us: 1.02x slower                                                   |
| xml_etree_parse      | 60.5 ms                                                                  | 64.3 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (3): json_loads, xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.77 ms                                                                  | 8.72 ms: 1.01x faster                                                   |
| python_startup_no_site | 6.32 ms                                                                  | 6.30 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 20.7 ms                                                                  | 20.0 ms: 1.03x faster                                                   |
| django_template | 13.8 ms                                                                  | 13.6 ms: 1.02x faster                                                   |
| genshi_text     | 8.81 ms                                                                  | 8.67 ms: 1.02x faster                                                   |
| mako            | 3.89 ms                                                                  | 3.86 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                                    | 1.02x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pprint_pformat                   | 532 ms                                                                   | 503 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 262 ms                                                                   | 250 ms: 1.05x faster                                                    |
| mdp                              | 615 ms                                                                   | 591 ms: 1.04x faster                                                    |
| bpe_tokeniser                    | 1.84 sec                                                                 | 1.77 sec: 1.04x faster                                                  |
| fannkuch                         | 156 ms                                                                   | 150 ms: 1.04x faster                                                    |
| many_optionals                   | 252 us                                                                   | 244 us: 1.04x faster                                                    |
| genshi_xml                       | 20.7 ms                                                                  | 20.0 ms: 1.03x faster                                                   |
| subparsers                       | 3.92 ms                                                                  | 3.81 ms: 1.03x faster                                                   |
| 2to3                             | 111 ms                                                                   | 109 ms: 1.03x faster                                                    |
| async_generators                 | 183 ms                                                                   | 179 ms: 1.03x faster                                                    |
| hexiom                           | 2.70 ms                                                                  | 2.64 ms: 1.03x faster                                                   |
| comprehensions                   | 6.32 us                                                                  | 6.17 us: 1.02x faster                                                   |
| meteor_contest                   | 45.7 ms                                                                  | 44.6 ms: 1.02x faster                                                   |
| pickle_pure_python               | 113 us                                                                   | 111 us: 1.02x faster                                                    |
| xml_etree_process                | 22.1 ms                                                                  | 21.6 ms: 1.02x faster                                                   |
| crypto_pyaes                     | 31.4 ms                                                                  | 30.7 ms: 1.02x faster                                                   |
| async_tree_eager_tg              | 77.4 ms                                                                  | 75.9 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 215 ms: 1.02x faster                                                    |
| async_tree_none                  | 96.4 ms                                                                  | 94.7 ms: 1.02x faster                                                   |
| dulwich_log                      | 18.8 ms                                                                  | 18.4 ms: 1.02x faster                                                   |
| xml_etree_generate               | 31.3 ms                                                                  | 30.8 ms: 1.02x faster                                                   |
| regex_compile                    | 40.8 ms                                                                  | 40.1 ms: 1.02x faster                                                   |
| telco                            | 2.64 ms                                                                  | 2.59 ms: 1.02x faster                                                   |
| richards                         | 9.33 ms                                                                  | 9.18 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed          | 245 ms                                                                   | 241 ms: 1.02x faster                                                    |
| django_template                  | 13.8 ms                                                                  | 13.6 ms: 1.02x faster                                                   |
| async_tree_eager                 | 37.3 ms                                                                  | 36.7 ms: 1.02x faster                                                   |
| genshi_text                      | 8.81 ms                                                                  | 8.67 ms: 1.02x faster                                                   |
| bench_mp_pool                    | 44.9 ms                                                                  | 44.2 ms: 1.02x faster                                                   |
| coroutines                       | 10.2 ms                                                                  | 10.1 ms: 1.02x faster                                                   |
| async_tree_io                    | 226 ms                                                                   | 222 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 251 ms                                                                   | 247 ms: 1.01x faster                                                    |
| deepcopy                         | 92.8 us                                                                  | 91.5 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 238 ms                                                                   | 235 ms: 1.01x faster                                                    |
| raytrace                         | 106 ms                                                                   | 105 ms: 1.01x faster                                                    |
| chaos                            | 21.9 ms                                                                  | 21.6 ms: 1.01x faster                                                   |
| create_gc_cycles                 | 910 us                                                                   | 898 us: 1.01x faster                                                    |
| json                             | 1.84 ms                                                                  | 1.82 ms: 1.01x faster                                                   |
| coverage                         | 32.8 ms                                                                  | 32.4 ms: 1.01x faster                                                   |
| asyncio_websockets               | 186 ms                                                                   | 184 ms: 1.01x faster                                                    |
| json_dumps                       | 3.63 ms                                                                  | 3.60 ms: 1.01x faster                                                   |
| deltablue                        | 1.14 ms                                                                  | 1.13 ms: 1.01x faster                                                   |
| logging_silent                   | 35.3 ns                                                                  | 35.0 ns: 1.01x faster                                                   |
| typing_runtime_protocols         | 62.2 us                                                                  | 61.7 us: 1.01x faster                                                   |
| deepcopy_reduce                  | 983 ns                                                                   | 974 ns: 1.01x faster                                                    |
| docutils                         | 992 ms                                                                   | 983 ms: 1.01x faster                                                    |
| richards_super                   | 11.2 ms                                                                  | 11.1 ms: 1.01x faster                                                   |
| mako                             | 3.89 ms                                                                  | 3.86 ms: 1.01x faster                                                   |
| pidigits                         | 160 ms                                                                   | 159 ms: 1.01x faster                                                    |
| async_tree_eager_memoization     | 105 ms                                                                   | 105 ms: 1.01x faster                                                    |
| logging_format                   | 2.30 us                                                                  | 2.29 us: 1.01x faster                                                   |
| python_startup                   | 8.77 ms                                                                  | 8.72 ms: 1.01x faster                                                   |
| spectral_norm                    | 39.4 ms                                                                  | 39.2 ms: 1.00x faster                                                   |
| logging_simple                   | 2.09 us                                                                  | 2.09 us: 1.00x faster                                                   |
| pathlib                          | 10.6 ms                                                                  | 10.6 ms: 1.00x faster                                                   |
| nqueens                          | 35.6 ms                                                                  | 35.5 ms: 1.00x faster                                                   |
| python_startup_no_site           | 6.32 ms                                                                  | 6.30 ms: 1.00x faster                                                   |
| sqlglot_v2_normalize             | 46.4 ms                                                                  | 46.3 ms: 1.00x faster                                                   |
| connected_components             | 197 ms                                                                   | 196 ms: 1.00x faster                                                    |
| scimark_sparse_mat_mult          | 1.86 ms                                                                  | 1.87 ms: 1.00x slower                                                   |
| thrift                           | 300 us                                                                   | 301 us: 1.00x slower                                                    |
| generators                       | 18.5 ms                                                                  | 18.6 ms: 1.01x slower                                                   |
| scimark_fft                      | 97.5 ms                                                                  | 98.2 ms: 1.01x slower                                                   |
| sympy_expand                     | 174 ms                                                                   | 176 ms: 1.01x slower                                                    |
| scimark_sor                      | 38.2 ms                                                                  | 38.6 ms: 1.01x slower                                                   |
| scimark_lu                       | 27.7 ms                                                                  | 28.0 ms: 1.01x slower                                                   |
| regex_effbot                     | 1.43 ms                                                                  | 1.45 ms: 1.01x slower                                                   |
| sympy_str                        | 106 ms                                                                   | 107 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.58 ms                                                                  | 7.68 ms: 1.01x slower                                                   |
| go                               | 45.7 ms                                                                  | 46.5 ms: 1.02x slower                                                   |
| unpickle_pure_python             | 74.0 us                                                                  | 75.4 us: 1.02x slower                                                   |
| regex_dna                        | 93.6 ms                                                                  | 95.8 ms: 1.02x slower                                                   |
| sympy_sum                        | 56.9 ms                                                                  | 58.7 ms: 1.03x slower                                                   |
| regex_v8                         | 9.50 ms                                                                  | 9.83 ms: 1.03x slower                                                   |
| pylint                           | 121 ms                                                                   | 126 ms: 1.04x slower                                                    |
| html5lib                         | 19.2 ms                                                                  | 20.1 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 60.5 ms                                                                  | 64.3 ms: 1.06x slower                                                   |
| sqlglot_v2_optimize              | 23.7 ms                                                                  | 25.4 ms: 1.07x slower                                                   |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (25): async_tree_eager_io, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_eager_memoization_tg, deepcopy_memo, gc_traversal, sqlite_synth, sqlglot_v2_parse, async_tree_eager_io_tg, pycparser, scimark_monte_carlo, nbody, bench_thread_pool, k_core, json_loads, xml_etree_iterparse, sqlglot_v2_transpile, shortest_path, pyflate, dask, sphinx, tomli_loads, float

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x