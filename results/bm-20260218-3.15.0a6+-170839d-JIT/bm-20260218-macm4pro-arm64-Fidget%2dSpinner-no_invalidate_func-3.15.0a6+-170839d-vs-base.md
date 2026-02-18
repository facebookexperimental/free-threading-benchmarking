# Results vs. base

- fork: Fidget-Spinner
- ref: no_invalidate_func
- machine: darwin-arm64
- commit hash: 170839d
- commit date: 2026-02-18
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 111 ms                                                                   | 111 ms: 1.00x slower                                                             |
| docutils       | 1.00 sec                                                                 | 1.03 sec: 1.03x slower                                                           |
| html5lib       | 19.8 ms                                                                  | 20.5 ms: 1.04x slower                                                            |
| sphinx         | 381 ms                                                                   | 395 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_memoization     | 106 ms                                                                   | 105 ms: 1.01x faster                                                             |
| coroutines                       | 10.2 ms                                                                  | 10.3 ms: 1.01x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 233 ms                                                                   | 236 ms: 1.01x slower                                                             |
| asyncio_websockets               | 186 ms                                                                   | 188 ms: 1.01x slower                                                             |
| async_tree_eager_memoization_tg  | 118 ms                                                                   | 119 ms: 1.01x slower                                                             |
| async_tree_memoization_tg        | 132 ms                                                                   | 134 ms: 1.01x slower                                                             |
| async_generators                 | 181 ms                                                                   | 184 ms: 1.01x slower                                                             |
| async_tree_eager_tg              | 77.5 ms                                                                  | 78.6 ms: 1.01x slower                                                            |
| async_tree_none_tg               | 93.5 ms                                                                  | 95.0 ms: 1.02x slower                                                            |
| async_tree_eager_io_tg           | 214 ms                                                                   | 219 ms: 1.02x slower                                                             |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                                     |

Benchmark hidden because not significant (9): async_tree_eager_cpu_io_mixed, async_tree_none, async_tree_eager, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_eager_io, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 39.8 ms                                                                  | 40.0 ms: 1.01x slower                                                            |
| float          | 23.7 ms                                                                  | 24.0 ms: 1.01x slower                                                            |
| pidigits       | 158 ms                                                                   | 167 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 39.5 ms                                                                  | 40.4 ms: 1.02x slower                                                            |
| regex_effbot   | 1.43 ms                                                                  | 1.48 ms: 1.04x slower                                                            |
| regex_v8       | 9.41 ms                                                                  | 9.76 ms: 1.04x slower                                                            |
| regex_dna      | 93.3 ms                                                                  | 98.0 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                                    | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 124 us                                                                   | 126 us: 1.01x slower                                                             |
| unpickle_pure_python | 83.2 us                                                                  | 84.8 us: 1.02x slower                                                            |
| xml_etree_parse      | 62.8 ms                                                                  | 64.1 ms: 1.02x slower                                                            |
| xml_etree_iterparse  | 38.3 ms                                                                  | 39.1 ms: 1.02x slower                                                            |
| json_loads           | 10.4 us                                                                  | 10.7 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                     |

Benchmark hidden because not significant (4): tomli_loads, json_dumps, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.33 ms                                                                  | 6.55 ms: 1.03x slower                                                            |
| python_startup         | 8.74 ms                                                                  | 9.08 ms: 1.04x slower                                                            |
| Geometric mean         | (ref)                                                                    | 1.04x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 13.6 ms                                                                  | 13.8 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| sqlglot_v2_optimize              | 24.1 ms                                                                  | 21.9 ms: 1.10x faster                                                            |
| hexiom                           | 2.66 ms                                                                  | 2.44 ms: 1.09x faster                                                            |
| sympy_str                        | 106 ms                                                                   | 98.3 ms: 1.07x faster                                                            |
| mdp                              | 572 ms                                                                   | 535 ms: 1.07x faster                                                             |
| comprehensions                   | 6.25 us                                                                  | 5.86 us: 1.07x faster                                                            |
| subparsers                       | 3.82 ms                                                                  | 3.61 ms: 1.06x faster                                                            |
| sympy_expand                     | 174 ms                                                                   | 167 ms: 1.04x faster                                                             |
| sqlglot_v2_normalize             | 47.2 ms                                                                  | 45.3 ms: 1.04x faster                                                            |
| nqueens                          | 35.8 ms                                                                  | 34.4 ms: 1.04x faster                                                            |
| many_optionals                   | 247 us                                                                   | 237 us: 1.04x faster                                                             |
| sympy_sum                        | 56.5 ms                                                                  | 54.7 ms: 1.03x faster                                                            |
| sympy_integrate                  | 7.55 ms                                                                  | 7.44 ms: 1.02x faster                                                            |
| async_tree_eager_memoization     | 106 ms                                                                   | 105 ms: 1.01x faster                                                             |
| connected_components             | 196 ms                                                                   | 196 ms: 1.00x faster                                                             |
| scimark_fft                      | 98.1 ms                                                                  | 97.8 ms: 1.00x faster                                                            |
| 2to3                             | 111 ms                                                                   | 111 ms: 1.00x slower                                                             |
| scimark_sparse_mat_mult          | 1.84 ms                                                                  | 1.84 ms: 1.00x slower                                                            |
| pprint_pformat                   | 508 ms                                                                   | 510 ms: 1.00x slower                                                             |
| typing_runtime_protocols         | 63.6 us                                                                  | 64.0 us: 1.01x slower                                                            |
| nbody                            | 39.8 ms                                                                  | 40.0 ms: 1.01x slower                                                            |
| logging_silent                   | 35.1 ns                                                                  | 35.3 ns: 1.01x slower                                                            |
| k_core                           | 859 ms                                                                   | 865 ms: 1.01x slower                                                             |
| bpe_tokeniser                    | 1.82 sec                                                                 | 1.84 sec: 1.01x slower                                                           |
| pprint_safe_repr                 | 252 ms                                                                   | 254 ms: 1.01x slower                                                             |
| coroutines                       | 10.2 ms                                                                  | 10.3 ms: 1.01x slower                                                            |
| scimark_sor                      | 39.0 ms                                                                  | 39.4 ms: 1.01x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 233 ms                                                                   | 236 ms: 1.01x slower                                                             |
| sqlite_synth                     | 933 ns                                                                   | 943 ns: 1.01x slower                                                             |
| float                            | 23.7 ms                                                                  | 24.0 ms: 1.01x slower                                                            |
| scimark_monte_carlo              | 22.8 ms                                                                  | 23.0 ms: 1.01x slower                                                            |
| crypto_pyaes                     | 31.5 ms                                                                  | 31.9 ms: 1.01x slower                                                            |
| asyncio_websockets               | 186 ms                                                                   | 188 ms: 1.01x slower                                                             |
| django_template                  | 13.6 ms                                                                  | 13.8 ms: 1.01x slower                                                            |
| chaos                            | 22.2 ms                                                                  | 22.5 ms: 1.01x slower                                                            |
| async_tree_eager_memoization_tg  | 118 ms                                                                   | 119 ms: 1.01x slower                                                             |
| pickle_pure_python               | 124 us                                                                   | 126 us: 1.01x slower                                                             |
| telco                            | 2.57 ms                                                                  | 2.60 ms: 1.01x slower                                                            |
| async_tree_memoization_tg        | 132 ms                                                                   | 134 ms: 1.01x slower                                                             |
| async_generators                 | 181 ms                                                                   | 184 ms: 1.01x slower                                                             |
| async_tree_eager_tg              | 77.5 ms                                                                  | 78.6 ms: 1.01x slower                                                            |
| deepcopy_memo                    | 10.3 us                                                                  | 10.4 us: 1.02x slower                                                            |
| async_tree_none_tg               | 93.5 ms                                                                  | 95.0 ms: 1.02x slower                                                            |
| sqlglot_v2_transpile             | 566 us                                                                   | 576 us: 1.02x slower                                                             |
| deepcopy                         | 92.5 us                                                                  | 94.1 us: 1.02x slower                                                            |
| deepcopy_reduce                  | 977 ns                                                                   | 994 ns: 1.02x slower                                                             |
| deltablue                        | 1.14 ms                                                                  | 1.16 ms: 1.02x slower                                                            |
| unpickle_pure_python             | 83.2 us                                                                  | 84.8 us: 1.02x slower                                                            |
| richards_super                   | 11.1 ms                                                                  | 11.3 ms: 1.02x slower                                                            |
| raytrace                         | 110 ms                                                                   | 113 ms: 1.02x slower                                                             |
| xml_etree_parse                  | 62.8 ms                                                                  | 64.1 ms: 1.02x slower                                                            |
| xml_etree_iterparse              | 38.3 ms                                                                  | 39.1 ms: 1.02x slower                                                            |
| regex_compile                    | 39.5 ms                                                                  | 40.4 ms: 1.02x slower                                                            |
| async_tree_eager_io_tg           | 214 ms                                                                   | 219 ms: 1.02x slower                                                             |
| generators                       | 18.3 ms                                                                  | 18.8 ms: 1.02x slower                                                            |
| pyflate                          | 148 ms                                                                   | 152 ms: 1.02x slower                                                             |
| pathlib                          | 10.5 ms                                                                  | 10.8 ms: 1.02x slower                                                            |
| bench_mp_pool                    | 44.6 ms                                                                  | 45.7 ms: 1.02x slower                                                            |
| logging_simple                   | 2.10 us                                                                  | 2.15 us: 1.03x slower                                                            |
| sqlglot_v2_parse                 | 442 us                                                                   | 455 us: 1.03x slower                                                             |
| richards                         | 9.27 ms                                                                  | 9.54 ms: 1.03x slower                                                            |
| json_loads                       | 10.4 us                                                                  | 10.7 us: 1.03x slower                                                            |
| logging_format                   | 2.29 us                                                                  | 2.36 us: 1.03x slower                                                            |
| meteor_contest                   | 44.5 ms                                                                  | 45.8 ms: 1.03x slower                                                            |
| docutils                         | 1.00 sec                                                                 | 1.03 sec: 1.03x slower                                                           |
| json                             | 1.80 ms                                                                  | 1.86 ms: 1.03x slower                                                            |
| coverage                         | 32.6 ms                                                                  | 33.7 ms: 1.03x slower                                                            |
| pycparser                        | 424 ms                                                                   | 438 ms: 1.03x slower                                                             |
| dulwich_log                      | 18.4 ms                                                                  | 19.0 ms: 1.03x slower                                                            |
| python_startup_no_site           | 6.33 ms                                                                  | 6.55 ms: 1.03x slower                                                            |
| regex_effbot                     | 1.43 ms                                                                  | 1.48 ms: 1.04x slower                                                            |
| go                               | 46.2 ms                                                                  | 47.8 ms: 1.04x slower                                                            |
| regex_v8                         | 9.41 ms                                                                  | 9.76 ms: 1.04x slower                                                            |
| sphinx                           | 381 ms                                                                   | 395 ms: 1.04x slower                                                             |
| html5lib                         | 19.8 ms                                                                  | 20.5 ms: 1.04x slower                                                            |
| python_startup                   | 8.74 ms                                                                  | 9.08 ms: 1.04x slower                                                            |
| gc_traversal                     | 2.01 ms                                                                  | 2.09 ms: 1.04x slower                                                            |
| create_gc_cycles                 | 888 us                                                                   | 932 us: 1.05x slower                                                             |
| regex_dna                        | 93.3 ms                                                                  | 98.0 ms: 1.05x slower                                                            |
| pidigits                         | 158 ms                                                                   | 167 ms: 1.06x slower                                                             |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                                     |

Benchmark hidden because not significant (22): pylint, tomli_loads, async_tree_eager_cpu_io_mixed, async_tree_none, bench_thread_pool, json_dumps, scimark_lu, spectral_norm, xml_etree_generate, dask, mako, fannkuch, shortest_path, xml_etree_process, thrift, async_tree_eager, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_eager_io, async_tree_io, async_tree_io_tg
Ignored benchmarks (8) of results/bm-20260214-3.15.0a6+-645f5c4-JIT/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x