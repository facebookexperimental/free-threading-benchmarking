# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 2e9b980
- commit date: 2026-03-15
- overall geometric mean: 1.025x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                   | 111 ms: 1.03x faster                                                         |
| docutils       | 990 ms                                                                   | 962 ms: 1.03x faster                                                         |
| html5lib       | 20.2 ms                                                                  | 18.8 ms: 1.07x faster                                                        |
| sphinx         | 391 ms                                                                   | 386 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| coroutines                       | 10.2 ms                                                                  | 9.35 ms: 1.09x faster                                                        |
| async_tree_io                    | 222 ms                                                                   | 207 ms: 1.07x faster                                                         |
| async_tree_none_tg               | 95.6 ms                                                                  | 89.4 ms: 1.07x faster                                                        |
| async_tree_none                  | 93.9 ms                                                                  | 88.2 ms: 1.06x faster                                                        |
| async_tree_eager_io_tg           | 215 ms                                                                   | 203 ms: 1.06x faster                                                         |
| async_tree_io_tg                 | 219 ms                                                                   | 207 ms: 1.06x faster                                                         |
| async_tree_eager_io              | 218 ms                                                                   | 207 ms: 1.05x faster                                                         |
| async_tree_eager_tg              | 80.6 ms                                                                  | 76.7 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 133 ms                                                                   | 127 ms: 1.05x faster                                                         |
| async_tree_memoization           | 131 ms                                                                   | 126 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 248 ms                                                                   | 238 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg  | 120 ms                                                                   | 115 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 237 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 234 ms: 1.03x faster                                                         |
| asyncio_websockets               | 188 ms                                                                   | 184 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 216 ms                                                                   | 212 ms: 1.02x faster                                                         |
| async_generators                 | 185 ms                                                                   | 183 ms: 1.01x faster                                                         |
| async_tree_eager_memoization     | 103 ms                                                                   | 102 ms: 1.01x faster                                                         |
| Geometric mean                   | (ref)                                                                    | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 164 ms                                                                   | 159 ms: 1.03x faster                                                         |
| nbody          | 40.2 ms                                                                  | 39.8 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 97.5 ms                                                                  | 93.2 ms: 1.05x faster                                                        |
| regex_v8       | 9.92 ms                                                                  | 9.53 ms: 1.04x faster                                                        |
| regex_effbot   | 1.51 ms                                                                  | 1.46 ms: 1.03x faster                                                        |
| regex_compile  | 40.5 ms                                                                  | 39.5 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_process    | 22.1 ms                                                                  | 21.5 ms: 1.03x faster                                                        |
| json_dumps           | 3.57 ms                                                                  | 3.51 ms: 1.02x faster                                                        |
| tomli_loads          | 636 ms                                                                   | 628 ms: 1.01x faster                                                         |
| json_loads           | 10.7 us                                                                  | 10.6 us: 1.01x faster                                                        |
| unpickle_pure_python | 85.4 us                                                                  | 84.9 us: 1.01x faster                                                        |
| pickle_pure_python   | 127 us                                                                   | 126 us: 1.01x faster                                                         |
| xml_etree_generate   | 31.3 ms                                                                  | 32.1 ms: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.32 ms                                                                  | 6.24 ms: 1.01x faster                                                        |
| python_startup         | 8.77 ms                                                                  | 8.68 ms: 1.01x faster                                                        |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.7 ms                                                                  | 12.4 ms: 1.11x faster                                                        |
| mako            | 4.03 ms                                                                  | 4.00 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                                    | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format                   | 2.34 us                                                                  | 1.91 us: 1.23x faster                                                        |
| logging_simple                   | 2.13 us                                                                  | 1.76 us: 1.21x faster                                                        |
| django_template                  | 13.7 ms                                                                  | 12.4 ms: 1.11x faster                                                        |
| coroutines                       | 10.2 ms                                                                  | 9.35 ms: 1.09x faster                                                        |
| html5lib                         | 20.2 ms                                                                  | 18.8 ms: 1.07x faster                                                        |
| async_tree_io                    | 222 ms                                                                   | 207 ms: 1.07x faster                                                         |
| async_tree_none_tg               | 95.6 ms                                                                  | 89.4 ms: 1.07x faster                                                        |
| async_tree_none                  | 93.9 ms                                                                  | 88.2 ms: 1.06x faster                                                        |
| async_tree_eager_io_tg           | 215 ms                                                                   | 203 ms: 1.06x faster                                                         |
| many_optionals                   | 237 us                                                                   | 224 us: 1.06x faster                                                         |
| sqlglot_v2_normalize             | 45.5 ms                                                                  | 43.0 ms: 1.06x faster                                                        |
| async_tree_io_tg                 | 219 ms                                                                   | 207 ms: 1.06x faster                                                         |
| chaos                            | 22.2 ms                                                                  | 21.0 ms: 1.06x faster                                                        |
| deltablue                        | 1.17 ms                                                                  | 1.11 ms: 1.05x faster                                                        |
| async_tree_eager_io              | 218 ms                                                                   | 207 ms: 1.05x faster                                                         |
| async_tree_eager_tg              | 80.6 ms                                                                  | 76.7 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 133 ms                                                                   | 127 ms: 1.05x faster                                                         |
| scimark_sor                      | 38.5 ms                                                                  | 36.8 ms: 1.05x faster                                                        |
| regex_dna                        | 97.5 ms                                                                  | 93.2 ms: 1.05x faster                                                        |
| async_tree_memoization           | 131 ms                                                                   | 126 ms: 1.04x faster                                                         |
| sqlglot_v2_optimize              | 22.0 ms                                                                  | 21.1 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 248 ms                                                                   | 238 ms: 1.04x faster                                                         |
| regex_v8                         | 9.92 ms                                                                  | 9.53 ms: 1.04x faster                                                        |
| pyflate                          | 151 ms                                                                   | 145 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg  | 120 ms                                                                   | 115 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 237 ms: 1.04x faster                                                         |
| sqlglot_v2_transpile             | 571 us                                                                   | 550 us: 1.04x faster                                                         |
| generators                       | 19.0 ms                                                                  | 18.3 ms: 1.04x faster                                                        |
| regex_effbot                     | 1.51 ms                                                                  | 1.46 ms: 1.03x faster                                                        |
| gc_traversal                     | 2.05 ms                                                                  | 1.99 ms: 1.03x faster                                                        |
| dulwich_log                      | 18.5 ms                                                                  | 17.9 ms: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                                   | 111 ms: 1.03x faster                                                         |
| create_gc_cycles                 | 910 us                                                                   | 881 us: 1.03x faster                                                         |
| pidigits                         | 164 ms                                                                   | 159 ms: 1.03x faster                                                         |
| docutils                         | 990 ms                                                                   | 962 ms: 1.03x faster                                                         |
| xml_etree_process                | 22.1 ms                                                                  | 21.5 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 234 ms: 1.03x faster                                                         |
| regex_compile                    | 40.5 ms                                                                  | 39.5 ms: 1.03x faster                                                        |
| meteor_contest                   | 45.9 ms                                                                  | 44.8 ms: 1.03x faster                                                        |
| typing_runtime_protocols         | 63.7 us                                                                  | 62.2 us: 1.03x faster                                                        |
| thrift                           | 310 us                                                                   | 303 us: 1.02x faster                                                         |
| mdp                              | 536 ms                                                                   | 523 ms: 1.02x faster                                                         |
| bench_mp_pool                    | 45.0 ms                                                                  | 44.0 ms: 1.02x faster                                                        |
| asyncio_websockets               | 188 ms                                                                   | 184 ms: 1.02x faster                                                         |
| sqlglot_v2_parse                 | 450 us                                                                   | 440 us: 1.02x faster                                                         |
| scimark_monte_carlo              | 23.3 ms                                                                  | 22.9 ms: 1.02x faster                                                        |
| subparsers                       | 3.56 ms                                                                  | 3.50 ms: 1.02x faster                                                        |
| json_dumps                       | 3.57 ms                                                                  | 3.51 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 216 ms                                                                   | 212 ms: 1.02x faster                                                         |
| coverage                         | 33.3 ms                                                                  | 32.8 ms: 1.02x faster                                                        |
| sympy_expand                     | 169 ms                                                                   | 166 ms: 1.02x faster                                                         |
| pathlib                          | 10.6 ms                                                                  | 10.5 ms: 1.02x faster                                                        |
| async_generators                 | 185 ms                                                                   | 183 ms: 1.01x faster                                                         |
| tomli_loads                      | 636 ms                                                                   | 628 ms: 1.01x faster                                                         |
| python_startup_no_site           | 6.32 ms                                                                  | 6.24 ms: 1.01x faster                                                        |
| sphinx                           | 391 ms                                                                   | 386 ms: 1.01x faster                                                         |
| nbody                            | 40.2 ms                                                                  | 39.8 ms: 1.01x faster                                                        |
| sympy_sum                        | 54.8 ms                                                                  | 54.2 ms: 1.01x faster                                                        |
| go                               | 46.4 ms                                                                  | 45.9 ms: 1.01x faster                                                        |
| python_startup                   | 8.77 ms                                                                  | 8.68 ms: 1.01x faster                                                        |
| crypto_pyaes                     | 31.9 ms                                                                  | 31.6 ms: 1.01x faster                                                        |
| async_tree_eager_memoization     | 103 ms                                                                   | 102 ms: 1.01x faster                                                         |
| json_loads                       | 10.7 us                                                                  | 10.6 us: 1.01x faster                                                        |
| sympy_str                        | 100 ms                                                                   | 99.5 ms: 1.01x faster                                                        |
| hexiom                           | 2.44 ms                                                                  | 2.42 ms: 1.01x faster                                                        |
| mako                             | 4.03 ms                                                                  | 4.00 ms: 1.01x faster                                                        |
| deepcopy                         | 94.9 us                                                                  | 94.3 us: 1.01x faster                                                        |
| unpickle_pure_python             | 85.4 us                                                                  | 84.9 us: 1.01x faster                                                        |
| pickle_pure_python               | 127 us                                                                   | 126 us: 1.01x faster                                                         |
| shortest_path                    | 215 ms                                                                   | 216 ms: 1.00x slower                                                         |
| spectral_norm                    | 37.9 ms                                                                  | 38.1 ms: 1.00x slower                                                        |
| comprehensions                   | 5.87 us                                                                  | 5.90 us: 1.01x slower                                                        |
| scimark_sparse_mat_mult          | 1.85 ms                                                                  | 1.86 ms: 1.01x slower                                                        |
| bench_thread_pool                | 429 us                                                                   | 433 us: 1.01x slower                                                         |
| nqueens                          | 32.0 ms                                                                  | 32.3 ms: 1.01x slower                                                        |
| fannkuch                         | 149 ms                                                                   | 150 ms: 1.01x slower                                                         |
| scimark_lu                       | 28.5 ms                                                                  | 28.9 ms: 1.01x slower                                                        |
| richards                         | 9.46 ms                                                                  | 9.63 ms: 1.02x slower                                                        |
| richards_super                   | 11.2 ms                                                                  | 11.4 ms: 1.02x slower                                                        |
| sympy_integrate                  | 7.44 ms                                                                  | 7.60 ms: 1.02x slower                                                        |
| xml_etree_generate               | 31.3 ms                                                                  | 32.1 ms: 1.02x slower                                                        |
| scimark_fft                      | 97.3 ms                                                                  | 101 ms: 1.04x slower                                                         |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                                 |

Benchmark hidden because not significant (19): pycparser, pprint_safe_repr, async_tree_eager, xml_etree_iterparse, dask, connected_components, float, k_core, bpe_tokeniser, raytrace, json, logging_silent, pylint, sqlite_synth, deepcopy_reduce, deepcopy_memo, pprint_pformat, telco, xml_etree_parse

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x