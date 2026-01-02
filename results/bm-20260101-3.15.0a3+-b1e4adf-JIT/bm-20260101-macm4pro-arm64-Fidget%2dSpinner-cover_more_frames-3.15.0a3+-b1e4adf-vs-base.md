# Results vs. base

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: darwin-arm64
- commit hash: b1e4adf
- commit date: 2026-01-01
- overall geometric mean: 1.009x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 112 ms: 1.02x slower                                                            |
| docutils       | 994 ms                                                                   | 1.02 sec: 1.03x slower                                                          |
| html5lib       | 19.9 ms                                                                  | 20.2 ms: 1.02x slower                                                           |
| sphinx         | 386 ms                                                                   | 391 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 219 ms: 1.01x slower                                                            |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 250 ms: 1.01x slower                                                            |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 255 ms: 1.01x slower                                                            |
| async_tree_none_tg               | 97.3 ms                                                                  | 98.6 ms: 1.01x slower                                                           |
| async_tree_eager_tg              | 78.4 ms                                                                  | 79.5 ms: 1.01x slower                                                           |
| async_tree_none                  | 98.2 ms                                                                  | 99.7 ms: 1.02x slower                                                           |
| async_generators                 | 182 ms                                                                   | 186 ms: 1.02x slower                                                            |
| async_tree_eager_io              | 219 ms                                                                   | 223 ms: 1.02x slower                                                            |
| coroutines                       | 10.0 ms                                                                  | 10.2 ms: 1.02x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 244 ms: 1.02x slower                                                            |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                                    |

Benchmark hidden because not significant (8): async_tree_eager, async_tree_io_tg, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_eager_memoization_tg, async_tree_eager_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 160 ms                                                                   | 164 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                    |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.44 ms                                                                  | 1.45 ms: 1.01x slower                                                           |
| regex_dna      | 94.2 ms                                                                  | 95.4 ms: 1.01x slower                                                           |
| regex_v8       | 9.61 ms                                                                  | 9.74 ms: 1.01x slower                                                           |
| regex_compile  | 39.5 ms                                                                  | 40.1 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 3.66 ms                                                                  | 3.68 ms: 1.01x slower                                                           |
| xml_etree_process    | 21.8 ms                                                                  | 21.9 ms: 1.01x slower                                                           |
| pickle_pure_python   | 111 us                                                                   | 113 us: 1.01x slower                                                            |
| tomli_loads          | 795 ms                                                                   | 809 ms: 1.02x slower                                                            |
| xml_etree_parse      | 59.2 ms                                                                  | 60.3 ms: 1.02x slower                                                           |
| unpickle_pure_python | 71.8 us                                                                  | 73.1 us: 1.02x slower                                                           |
| xml_etree_iterparse  | 36.2 ms                                                                  | 37.5 ms: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                    |

Benchmark hidden because not significant (2): xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.29 ms                                                                  | 6.38 ms: 1.01x slower                                                           |
| python_startup         | 8.73 ms                                                                  | 8.86 ms: 1.01x slower                                                           |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml     | 21.4 ms                                                                  | 20.5 ms: 1.04x faster                                                           |
| genshi_text    | 9.09 ms                                                                  | 8.89 ms: 1.02x faster                                                           |
| mako           | 3.89 ms                                                                  | 3.91 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml                       | 21.4 ms                                                                  | 20.5 ms: 1.04x faster                                                           |
| genshi_text                      | 9.09 ms                                                                  | 8.89 ms: 1.02x faster                                                           |
| telco                            | 2.58 ms                                                                  | 2.52 ms: 1.02x faster                                                           |
| sqlglot_v2_normalize             | 47.5 ms                                                                  | 46.8 ms: 1.01x faster                                                           |
| spectral_norm                    | 41.1 ms                                                                  | 40.8 ms: 1.01x faster                                                           |
| nqueens                          | 38.7 ms                                                                  | 38.4 ms: 1.01x faster                                                           |
| bench_thread_pool                | 428 us                                                                   | 426 us: 1.00x faster                                                            |
| sympy_expand                     | 173 ms                                                                   | 174 ms: 1.00x slower                                                            |
| connected_components             | 197 ms                                                                   | 198 ms: 1.01x slower                                                            |
| k_core                           | 862 ms                                                                   | 867 ms: 1.01x slower                                                            |
| shortest_path                    | 215 ms                                                                   | 217 ms: 1.01x slower                                                            |
| scimark_sparse_mat_mult          | 1.92 ms                                                                  | 1.93 ms: 1.01x slower                                                           |
| deltablue                        | 1.12 ms                                                                  | 1.12 ms: 1.01x slower                                                           |
| regex_effbot                     | 1.44 ms                                                                  | 1.45 ms: 1.01x slower                                                           |
| pprint_safe_repr                 | 257 ms                                                                   | 259 ms: 1.01x slower                                                            |
| mako                             | 3.89 ms                                                                  | 3.91 ms: 1.01x slower                                                           |
| json_dumps                       | 3.66 ms                                                                  | 3.68 ms: 1.01x slower                                                           |
| deepcopy                         | 97.1 us                                                                  | 97.8 us: 1.01x slower                                                           |
| deepcopy_memo                    | 11.4 us                                                                  | 11.5 us: 1.01x slower                                                           |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 219 ms: 1.01x slower                                                            |
| xml_etree_process                | 21.8 ms                                                                  | 21.9 ms: 1.01x slower                                                           |
| typing_runtime_protocols         | 61.8 us                                                                  | 62.3 us: 1.01x slower                                                           |
| scimark_lu                       | 36.1 ms                                                                  | 36.5 ms: 1.01x slower                                                           |
| pathlib                          | 10.8 ms                                                                  | 10.9 ms: 1.01x slower                                                           |
| raytrace                         | 106 ms                                                                   | 107 ms: 1.01x slower                                                            |
| scimark_sor                      | 41.7 ms                                                                  | 42.1 ms: 1.01x slower                                                           |
| hexiom                           | 2.60 ms                                                                  | 2.63 ms: 1.01x slower                                                           |
| bpe_tokeniser                    | 1.83 sec                                                                 | 1.85 sec: 1.01x slower                                                          |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 250 ms: 1.01x slower                                                            |
| chaos                            | 21.8 ms                                                                  | 22.0 ms: 1.01x slower                                                           |
| go                               | 42.7 ms                                                                  | 43.2 ms: 1.01x slower                                                           |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 255 ms: 1.01x slower                                                            |
| pickle_pure_python               | 111 us                                                                   | 113 us: 1.01x slower                                                            |
| gc_traversal                     | 2.05 ms                                                                  | 2.08 ms: 1.01x slower                                                           |
| regex_dna                        | 94.2 ms                                                                  | 95.4 ms: 1.01x slower                                                           |
| async_tree_none_tg               | 97.3 ms                                                                  | 98.6 ms: 1.01x slower                                                           |
| python_startup_no_site           | 6.29 ms                                                                  | 6.38 ms: 1.01x slower                                                           |
| logging_format                   | 2.29 us                                                                  | 2.32 us: 1.01x slower                                                           |
| sympy_sum                        | 55.9 ms                                                                  | 56.6 ms: 1.01x slower                                                           |
| sphinx                           | 386 ms                                                                   | 391 ms: 1.01x slower                                                            |
| regex_v8                         | 9.61 ms                                                                  | 9.74 ms: 1.01x slower                                                           |
| mdp                              | 577 ms                                                                   | 585 ms: 1.01x slower                                                            |
| async_tree_eager_tg              | 78.4 ms                                                                  | 79.5 ms: 1.01x slower                                                           |
| regex_compile                    | 39.5 ms                                                                  | 40.1 ms: 1.01x slower                                                           |
| subparsers                       | 3.87 ms                                                                  | 3.92 ms: 1.01x slower                                                           |
| python_startup                   | 8.73 ms                                                                  | 8.86 ms: 1.01x slower                                                           |
| crypto_pyaes                     | 30.7 ms                                                                  | 31.1 ms: 1.01x slower                                                           |
| pprint_pformat                   | 516 ms                                                                   | 524 ms: 1.02x slower                                                            |
| async_tree_none                  | 98.2 ms                                                                  | 99.7 ms: 1.02x slower                                                           |
| many_optionals                   | 252 us                                                                   | 256 us: 1.02x slower                                                            |
| thrift                           | 285 us                                                                   | 289 us: 1.02x slower                                                            |
| pycparser                        | 433 ms                                                                   | 440 ms: 1.02x slower                                                            |
| async_generators                 | 182 ms                                                                   | 186 ms: 1.02x slower                                                            |
| async_tree_eager_io              | 219 ms                                                                   | 223 ms: 1.02x slower                                                            |
| tomli_loads                      | 795 ms                                                                   | 809 ms: 1.02x slower                                                            |
| logging_simple                   | 2.07 us                                                                  | 2.11 us: 1.02x slower                                                           |
| scimark_fft                      | 99.2 ms                                                                  | 101 ms: 1.02x slower                                                            |
| xml_etree_parse                  | 59.2 ms                                                                  | 60.3 ms: 1.02x slower                                                           |
| meteor_contest                   | 44.8 ms                                                                  | 45.6 ms: 1.02x slower                                                           |
| html5lib                         | 19.9 ms                                                                  | 20.2 ms: 1.02x slower                                                           |
| bench_mp_pool                    | 44.8 ms                                                                  | 45.6 ms: 1.02x slower                                                           |
| unpickle_pure_python             | 71.8 us                                                                  | 73.1 us: 1.02x slower                                                           |
| pyflate                          | 142 ms                                                                   | 145 ms: 1.02x slower                                                            |
| richards                         | 9.59 ms                                                                  | 9.77 ms: 1.02x slower                                                           |
| json                             | 1.84 ms                                                                  | 1.88 ms: 1.02x slower                                                           |
| coroutines                       | 10.0 ms                                                                  | 10.2 ms: 1.02x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 244 ms: 1.02x slower                                                            |
| create_gc_cycles                 | 913 us                                                                   | 933 us: 1.02x slower                                                            |
| 2to3                             | 110 ms                                                                   | 112 ms: 1.02x slower                                                            |
| pidigits                         | 160 ms                                                                   | 164 ms: 1.02x slower                                                            |
| dulwich_log                      | 18.7 ms                                                                  | 19.2 ms: 1.02x slower                                                           |
| docutils                         | 994 ms                                                                   | 1.02 sec: 1.03x slower                                                          |
| sympy_integrate                  | 7.41 ms                                                                  | 7.60 ms: 1.03x slower                                                           |
| sqlglot_v2_parse                 | 447 us                                                                   | 459 us: 1.03x slower                                                            |
| sympy_str                        | 103 ms                                                                   | 106 ms: 1.03x slower                                                            |
| sqlglot_v2_transpile             | 570 us                                                                   | 585 us: 1.03x slower                                                            |
| xml_etree_iterparse              | 36.2 ms                                                                  | 37.5 ms: 1.03x slower                                                           |
| generators                       | 18.4 ms                                                                  | 19.0 ms: 1.04x slower                                                           |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                                    |

Benchmark hidden because not significant (23): fannkuch, async_tree_eager, xml_etree_generate, comprehensions, logging_silent, coverage, sqlglot_v2_optimize, deepcopy_reduce, sqlite_synth, nbody, float, async_tree_io_tg, scimark_monte_carlo, django_template, json_loads, richards_super, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_eager_memoization_tg, async_tree_eager_io_tg, pylint
Ignored benchmarks (1) of results/bm-20260101-3.15.0a3+-b1e4adf-JIT/bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x