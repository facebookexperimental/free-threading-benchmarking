# Results vs. base

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: darwin-arm64
- commit hash: 8f7b4f4
- commit date: 2026-01-02
- overall geometric mean: 1.015x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 107 ms: 1.03x faster                                                            |
| docutils       | 994 ms                                                                   | 980 ms: 1.02x faster                                                            |
| html5lib       | 19.9 ms                                                                  | 19.4 ms: 1.03x faster                                                           |
| sphinx         | 386 ms                                                                   | 382 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg                 | 222 ms                                                                   | 214 ms: 1.04x faster                                                            |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 231 ms: 1.04x faster                                                            |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 238 ms: 1.04x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 210 ms: 1.04x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 243 ms: 1.04x faster                                                            |
| async_tree_eager                 | 38.2 ms                                                                  | 37.0 ms: 1.03x faster                                                           |
| async_tree_eager_tg              | 78.4 ms                                                                  | 75.9 ms: 1.03x faster                                                           |
| async_tree_none                  | 98.2 ms                                                                  | 95.2 ms: 1.03x faster                                                           |
| async_tree_none_tg               | 97.3 ms                                                                  | 94.5 ms: 1.03x faster                                                           |
| async_generators                 | 182 ms                                                                   | 178 ms: 1.03x faster                                                            |
| async_tree_io                    | 229 ms                                                                   | 224 ms: 1.02x faster                                                            |
| async_tree_eager_io              | 219 ms                                                                   | 215 ms: 1.02x faster                                                            |
| async_tree_eager_memoization     | 105 ms                                                                   | 104 ms: 1.01x faster                                                            |
| coroutines                       | 10.0 ms                                                                  | 10.1 ms: 1.01x slower                                                           |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                                    |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_memoization, async_tree_eager_io_tg, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 160 ms                                                                   | 155 ms: 1.03x faster                                                            |
| nbody          | 39.8 ms                                                                  | 38.9 ms: 1.02x faster                                                           |
| float          | 23.0 ms                                                                  | 22.5 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 94.2 ms                                                                  | 91.8 ms: 1.03x faster                                                           |
| regex_effbot   | 1.44 ms                                                                  | 1.42 ms: 1.02x faster                                                           |
| regex_v8       | 9.61 ms                                                                  | 9.45 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|--------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_loads         | 10.7 us                                                                  | 10.4 us: 1.03x faster                                                           |
| pickle_pure_python | 111 us                                                                   | 110 us: 1.02x faster                                                            |
| json_dumps         | 3.66 ms                                                                  | 3.61 ms: 1.01x faster                                                           |
| xml_etree_generate | 30.8 ms                                                                  | 30.5 ms: 1.01x faster                                                           |
| xml_etree_process  | 21.8 ms                                                                  | 21.6 ms: 1.01x faster                                                           |
| tomli_loads        | 795 ms                                                                   | 788 ms: 1.01x faster                                                            |
| Geometric mean     | (ref)                                                                    | 1.01x faster                                                                    |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.73 ms                                                                  | 8.70 ms: 1.00x faster                                                           |
| python_startup_no_site | 6.29 ms                                                                  | 6.29 ms: 1.00x faster                                                           |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|-----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                                  | 19.7 ms: 1.08x faster                                                           |
| genshi_text     | 9.09 ms                                                                  | 8.71 ms: 1.04x faster                                                           |
| django_template | 13.9 ms                                                                  | 13.6 ms: 1.02x faster                                                           |
| mako            | 3.89 ms                                                                  | 3.83 ms: 1.02x faster                                                           |
| Geometric mean  | (ref)                                                                    | 1.04x faster                                                                    |

All benchmarks:
===============

| Benchmark                        | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml                       | 21.4 ms                                                                  | 19.7 ms: 1.08x faster                                                           |
| coverage                         | 33.8 ms                                                                  | 32.1 ms: 1.05x faster                                                           |
| many_optionals                   | 252 us                                                                   | 240 us: 1.05x faster                                                            |
| genshi_text                      | 9.09 ms                                                                  | 8.71 ms: 1.04x faster                                                           |
| async_tree_io_tg                 | 222 ms                                                                   | 214 ms: 1.04x faster                                                            |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 231 ms: 1.04x faster                                                            |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 238 ms: 1.04x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 210 ms: 1.04x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 243 ms: 1.04x faster                                                            |
| json_loads                       | 10.7 us                                                                  | 10.4 us: 1.03x faster                                                           |
| create_gc_cycles                 | 913 us                                                                   | 885 us: 1.03x faster                                                            |
| async_tree_eager                 | 38.2 ms                                                                  | 37.0 ms: 1.03x faster                                                           |
| async_tree_eager_tg              | 78.4 ms                                                                  | 75.9 ms: 1.03x faster                                                           |
| async_tree_none                  | 98.2 ms                                                                  | 95.2 ms: 1.03x faster                                                           |
| pidigits                         | 160 ms                                                                   | 155 ms: 1.03x faster                                                            |
| bench_mp_pool                    | 44.8 ms                                                                  | 43.5 ms: 1.03x faster                                                           |
| async_tree_none_tg               | 97.3 ms                                                                  | 94.5 ms: 1.03x faster                                                           |
| subparsers                       | 3.87 ms                                                                  | 3.76 ms: 1.03x faster                                                           |
| json                             | 1.84 ms                                                                  | 1.79 ms: 1.03x faster                                                           |
| richards_super                   | 11.6 ms                                                                  | 11.3 ms: 1.03x faster                                                           |
| 2to3                             | 110 ms                                                                   | 107 ms: 1.03x faster                                                            |
| regex_dna                        | 94.2 ms                                                                  | 91.8 ms: 1.03x faster                                                           |
| sqlglot_v2_normalize             | 47.5 ms                                                                  | 46.2 ms: 1.03x faster                                                           |
| async_generators                 | 182 ms                                                                   | 178 ms: 1.03x faster                                                            |
| html5lib                         | 19.9 ms                                                                  | 19.4 ms: 1.03x faster                                                           |
| generators                       | 18.4 ms                                                                  | 17.9 ms: 1.03x faster                                                           |
| dulwich_log                      | 18.7 ms                                                                  | 18.2 ms: 1.02x faster                                                           |
| gc_traversal                     | 2.05 ms                                                                  | 2.00 ms: 1.02x faster                                                           |
| go                               | 42.7 ms                                                                  | 41.7 ms: 1.02x faster                                                           |
| nbody                            | 39.8 ms                                                                  | 38.9 ms: 1.02x faster                                                           |
| async_tree_io                    | 229 ms                                                                   | 224 ms: 1.02x faster                                                            |
| nqueens                          | 38.7 ms                                                                  | 37.8 ms: 1.02x faster                                                           |
| pprint_safe_repr                 | 257 ms                                                                   | 251 ms: 1.02x faster                                                            |
| crypto_pyaes                     | 30.7 ms                                                                  | 30.0 ms: 1.02x faster                                                           |
| sqlglot_v2_optimize              | 23.8 ms                                                                  | 23.3 ms: 1.02x faster                                                           |
| float                            | 23.0 ms                                                                  | 22.5 ms: 1.02x faster                                                           |
| sqlite_synth                     | 963 ns                                                                   | 944 ns: 1.02x faster                                                            |
| deepcopy_memo                    | 11.4 us                                                                  | 11.2 us: 1.02x faster                                                           |
| regex_effbot                     | 1.44 ms                                                                  | 1.42 ms: 1.02x faster                                                           |
| pathlib                          | 10.8 ms                                                                  | 10.6 ms: 1.02x faster                                                           |
| async_tree_eager_io              | 219 ms                                                                   | 215 ms: 1.02x faster                                                            |
| chaos                            | 21.8 ms                                                                  | 21.4 ms: 1.02x faster                                                           |
| raytrace                         | 106 ms                                                                   | 104 ms: 1.02x faster                                                            |
| fannkuch                         | 153 ms                                                                   | 151 ms: 1.02x faster                                                            |
| comprehensions                   | 6.18 us                                                                  | 6.08 us: 1.02x faster                                                           |
| regex_v8                         | 9.61 ms                                                                  | 9.45 ms: 1.02x faster                                                           |
| pickle_pure_python               | 111 us                                                                   | 110 us: 1.02x faster                                                            |
| django_template                  | 13.9 ms                                                                  | 13.6 ms: 1.02x faster                                                           |
| logging_silent                   | 33.7 ns                                                                  | 33.2 ns: 1.02x faster                                                           |
| richards                         | 9.59 ms                                                                  | 9.44 ms: 1.02x faster                                                           |
| docutils                         | 994 ms                                                                   | 980 ms: 1.02x faster                                                            |
| mako                             | 3.89 ms                                                                  | 3.83 ms: 1.02x faster                                                           |
| pprint_pformat                   | 516 ms                                                                   | 509 ms: 1.01x faster                                                            |
| json_dumps                       | 3.66 ms                                                                  | 3.61 ms: 1.01x faster                                                           |
| spectral_norm                    | 41.1 ms                                                                  | 40.6 ms: 1.01x faster                                                           |
| async_tree_eager_memoization     | 105 ms                                                                   | 104 ms: 1.01x faster                                                            |
| deltablue                        | 1.12 ms                                                                  | 1.10 ms: 1.01x faster                                                           |
| pyflate                          | 142 ms                                                                   | 141 ms: 1.01x faster                                                            |
| sphinx                           | 386 ms                                                                   | 382 ms: 1.01x faster                                                            |
| bpe_tokeniser                    | 1.83 sec                                                                 | 1.81 sec: 1.01x faster                                                          |
| xml_etree_generate               | 30.8 ms                                                                  | 30.5 ms: 1.01x faster                                                           |
| xml_etree_process                | 21.8 ms                                                                  | 21.6 ms: 1.01x faster                                                           |
| scimark_sparse_mat_mult          | 1.92 ms                                                                  | 1.90 ms: 1.01x faster                                                           |
| hexiom                           | 2.60 ms                                                                  | 2.58 ms: 1.01x faster                                                           |
| typing_runtime_protocols         | 61.8 us                                                                  | 61.2 us: 1.01x faster                                                           |
| tomli_loads                      | 795 ms                                                                   | 788 ms: 1.01x faster                                                            |
| mdp                              | 577 ms                                                                   | 573 ms: 1.01x faster                                                            |
| scimark_monte_carlo              | 22.5 ms                                                                  | 22.3 ms: 1.01x faster                                                           |
| deepcopy                         | 97.1 us                                                                  | 96.4 us: 1.01x faster                                                           |
| meteor_contest                   | 44.8 ms                                                                  | 44.5 ms: 1.01x faster                                                           |
| telco                            | 2.58 ms                                                                  | 2.56 ms: 1.01x faster                                                           |
| sympy_sum                        | 55.9 ms                                                                  | 55.6 ms: 1.00x faster                                                           |
| python_startup                   | 8.73 ms                                                                  | 8.70 ms: 1.00x faster                                                           |
| python_startup_no_site           | 6.29 ms                                                                  | 6.29 ms: 1.00x faster                                                           |
| logging_format                   | 2.29 us                                                                  | 2.30 us: 1.00x slower                                                           |
| shortest_path                    | 215 ms                                                                   | 216 ms: 1.00x slower                                                            |
| logging_simple                   | 2.07 us                                                                  | 2.08 us: 1.01x slower                                                           |
| connected_components             | 197 ms                                                                   | 198 ms: 1.01x slower                                                            |
| sympy_integrate                  | 7.41 ms                                                                  | 7.45 ms: 1.01x slower                                                           |
| sympy_str                        | 103 ms                                                                   | 104 ms: 1.01x slower                                                            |
| coroutines                       | 10.0 ms                                                                  | 10.1 ms: 1.01x slower                                                           |
| scimark_fft                      | 99.2 ms                                                                  | 102 ms: 1.03x slower                                                            |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                                    |

Benchmark hidden because not significant (19): pylint, async_tree_memoization_tg, async_tree_memoization, async_tree_eager_io_tg, pycparser, async_tree_eager_memoization_tg, xml_etree_iterparse, deepcopy_reduce, thrift, bench_thread_pool, sympy_expand, unpickle_pure_python, k_core, sqlglot_v2_parse, sqlglot_v2_transpile, regex_compile, scimark_lu, xml_etree_parse, scimark_sor
Ignored benchmarks (1) of results/bm-20260102-3.15.0a3+-8f7b4f4-JIT/bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.99x