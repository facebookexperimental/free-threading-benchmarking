# Results vs. base

- fork: Yhg1s
- ref: uniqref_critsection
- machine: darwin-arm64
- commit hash: dd2ec59
- commit date: 2025-03-27
- overall geometric mean: 1.004x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 115 ms                                                                   | 112 ms: 1.02x faster                                                   |
| docutils       | 978 ms                                                                   | 967 ms: 1.01x faster                                                   |
| html5lib       | 22.5 ms                                                                  | 22.3 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none                  | 99.9 ms                                                                  | 98.1 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed          | 240 ms                                                                   | 236 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 231 ms                                                                   | 227 ms: 1.02x faster                                                   |
| async_tree_eager_io              | 199 ms                                                                   | 196 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 222 ms                                                                   | 219 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                   | 216 ms: 1.01x faster                                                   |
| async_tree_eager_tg              | 74.9 ms                                                                  | 74.0 ms: 1.01x faster                                                  |
| async_tree_eager_io_tg           | 186 ms                                                                   | 183 ms: 1.01x faster                                                   |
| asyncio_websockets               | 191 ms                                                                   | 189 ms: 1.01x faster                                                   |
| async_tree_eager                 | 46.7 ms                                                                  | 46.2 ms: 1.01x faster                                                  |
| async_generators                 | 169 ms                                                                   | 167 ms: 1.01x faster                                                   |
| async_tree_none_tg               | 83.2 ms                                                                  | 82.7 ms: 1.01x faster                                                  |
| async_tree_io                    | 205 ms                                                                   | 204 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 110 ms                                                                   | 109 ms: 1.01x faster                                                   |
| async_tree_memoization           | 129 ms                                                                   | 128 ms: 1.01x faster                                                   |
| async_tree_memoization_tg        | 121 ms                                                                   | 120 ms: 1.00x faster                                                   |
| async_tree_eager_memoization     | 108 ms                                                                   | 108 ms: 1.00x faster                                                   |
| async_tree_io_tg                 | 190 ms                                                                   | 189 ms: 1.00x faster                                                   |
| coroutines                       | 9.11 ms                                                                  | 9.17 ms: 1.01x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                                   | 163 ms: 1.02x faster                                                   |
| float          | 28.9 ms                                                                  | 28.8 ms: 1.00x faster                                                  |
| nbody          | 60.1 ms                                                                  | 61.3 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 103 ms                                                                   | 102 ms: 1.00x faster                                                   |
| regex_v8       | 10.1 ms                                                                  | 10.1 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_generate   | 34.8 ms                                                                  | 33.8 ms: 1.03x faster                                                  |
| json_loads           | 11.8 us                                                                  | 11.6 us: 1.01x faster                                                  |
| xml_etree_process    | 25.2 ms                                                                  | 24.9 ms: 1.01x faster                                                  |
| xml_etree_parse      | 57.1 ms                                                                  | 56.6 ms: 1.01x faster                                                  |
| json_dumps           | 5.09 ms                                                                  | 5.06 ms: 1.00x faster                                                  |
| unpickle_pure_python | 98.8 us                                                                  | 99.2 us: 1.00x slower                                                  |
| pickle_pure_python   | 140 us                                                                   | 141 us: 1.00x slower                                                   |
| xml_etree_iterparse  | 35.4 ms                                                                  | 36.4 ms: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.31 ms                                                                  | 9.21 ms: 1.01x faster                                                  |
| python_startup_no_site | 7.35 ms                                                                  | 7.28 ms: 1.01x faster                                                  |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 15.3 ms                                                                  | 15.2 ms: 1.01x faster                                                  |
| mako            | 5.47 ms                                                                  | 5.46 ms: 1.00x faster                                                  |
| Geometric mean  | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| many_optionals                   | 235 us                                                                   | 228 us: 1.03x faster                                                   |
| xml_etree_generate               | 34.8 ms                                                                  | 33.8 ms: 1.03x faster                                                  |
| richards                         | 22.9 ms                                                                  | 22.3 ms: 1.03x faster                                                  |
| json                             | 1.96 ms                                                                  | 1.92 ms: 1.02x faster                                                  |
| 2to3                             | 115 ms                                                                   | 112 ms: 1.02x faster                                                   |
| bench_mp_pool                    | 39.9 ms                                                                  | 39.1 ms: 1.02x faster                                                  |
| subparsers                       | 8.44 ms                                                                  | 8.29 ms: 1.02x faster                                                  |
| async_tree_none                  | 99.9 ms                                                                  | 98.1 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed          | 240 ms                                                                   | 236 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 231 ms                                                                   | 227 ms: 1.02x faster                                                   |
| async_tree_eager_io              | 199 ms                                                                   | 196 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                                   | 163 ms: 1.02x faster                                                   |
| json_loads                       | 11.8 us                                                                  | 11.6 us: 1.01x faster                                                  |
| bench_thread_pool                | 590 us                                                                   | 581 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 222 ms                                                                   | 219 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                   | 216 ms: 1.01x faster                                                   |
| create_gc_cycles                 | 464 us                                                                   | 458 us: 1.01x faster                                                   |
| async_tree_eager_tg              | 74.9 ms                                                                  | 74.0 ms: 1.01x faster                                                  |
| logging_silent                   | 43.3 ns                                                                  | 42.8 ns: 1.01x faster                                                  |
| async_tree_eager_io_tg           | 186 ms                                                                   | 183 ms: 1.01x faster                                                   |
| docutils                         | 978 ms                                                                   | 967 ms: 1.01x faster                                                   |
| python_startup                   | 9.31 ms                                                                  | 9.21 ms: 1.01x faster                                                  |
| asyncio_websockets               | 191 ms                                                                   | 189 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 33.5 ms                                                                  | 33.1 ms: 1.01x faster                                                  |
| dulwich_log                      | 18.0 ms                                                                  | 17.8 ms: 1.01x faster                                                  |
| python_startup_no_site           | 7.35 ms                                                                  | 7.28 ms: 1.01x faster                                                  |
| xml_etree_process                | 25.2 ms                                                                  | 24.9 ms: 1.01x faster                                                  |
| deepcopy                         | 110 us                                                                   | 109 us: 1.01x faster                                                   |
| async_tree_eager                 | 46.7 ms                                                                  | 46.2 ms: 1.01x faster                                                  |
| scimark_lu                       | 51.4 ms                                                                  | 50.9 ms: 1.01x faster                                                  |
| xml_etree_parse                  | 57.1 ms                                                                  | 56.6 ms: 1.01x faster                                                  |
| sqlalchemy_declarative           | 48.1 ms                                                                  | 47.6 ms: 1.01x faster                                                  |
| async_generators                 | 169 ms                                                                   | 167 ms: 1.01x faster                                                   |
| html5lib                         | 22.5 ms                                                                  | 22.3 ms: 1.01x faster                                                  |
| thrift                           | 311 us                                                                   | 309 us: 1.01x faster                                                   |
| richards_super                   | 25.8 ms                                                                  | 25.6 ms: 1.01x faster                                                  |
| connected_components             | 230 ms                                                                   | 229 ms: 1.01x faster                                                   |
| async_tree_none_tg               | 83.2 ms                                                                  | 82.7 ms: 1.01x faster                                                  |
| shortest_path                    | 239 ms                                                                   | 237 ms: 1.01x faster                                                   |
| django_template                  | 15.3 ms                                                                  | 15.2 ms: 1.01x faster                                                  |
| fannkuch                         | 189 ms                                                                   | 188 ms: 1.01x faster                                                   |
| async_tree_io                    | 205 ms                                                                   | 204 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 110 ms                                                                   | 109 ms: 1.01x faster                                                   |
| sqlalchemy_imperative            | 5.42 ms                                                                  | 5.39 ms: 1.01x faster                                                  |
| async_tree_memoization           | 129 ms                                                                   | 128 ms: 1.01x faster                                                   |
| json_dumps                       | 5.09 ms                                                                  | 5.06 ms: 1.00x faster                                                  |
| async_tree_memoization_tg        | 121 ms                                                                   | 120 ms: 1.00x faster                                                   |
| sqlglot_v2_parse                 | 561 us                                                                   | 559 us: 1.00x faster                                                   |
| regex_dna                        | 103 ms                                                                   | 102 ms: 1.00x faster                                                   |
| logging_simple                   | 2.38 us                                                                  | 2.37 us: 1.00x faster                                                  |
| async_tree_eager_memoization     | 108 ms                                                                   | 108 ms: 1.00x faster                                                   |
| crypto_pyaes                     | 39.9 ms                                                                  | 39.7 ms: 1.00x faster                                                  |
| logging_format                   | 2.61 us                                                                  | 2.60 us: 1.00x faster                                                  |
| float                            | 28.9 ms                                                                  | 28.8 ms: 1.00x faster                                                  |
| async_tree_io_tg                 | 190 ms                                                                   | 189 ms: 1.00x faster                                                   |
| mako                             | 5.47 ms                                                                  | 5.46 ms: 1.00x faster                                                  |
| hexiom                           | 2.93 ms                                                                  | 2.93 ms: 1.00x slower                                                  |
| pprint_safe_repr                 | 340 ms                                                                   | 341 ms: 1.00x slower                                                   |
| unpickle_pure_python             | 98.8 us                                                                  | 99.2 us: 1.00x slower                                                  |
| pickle_pure_python               | 140 us                                                                   | 141 us: 1.00x slower                                                   |
| raytrace                         | 129 ms                                                                   | 130 ms: 1.00x slower                                                   |
| pyflate                          | 195 ms                                                                   | 196 ms: 1.01x slower                                                   |
| chaos                            | 27.8 ms                                                                  | 28.0 ms: 1.01x slower                                                  |
| regex_v8                         | 10.1 ms                                                                  | 10.1 ms: 1.01x slower                                                  |
| coroutines                       | 9.11 ms                                                                  | 9.17 ms: 1.01x slower                                                  |
| sqlglot_v2_normalize             | 44.1 ms                                                                  | 44.4 ms: 1.01x slower                                                  |
| scimark_sor                      | 54.0 ms                                                                  | 54.4 ms: 1.01x slower                                                  |
| pprint_pformat                   | 691 ms                                                                   | 696 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 2.19 ms                                                                  | 2.21 ms: 1.01x slower                                                  |
| telco                            | 3.30 ms                                                                  | 3.34 ms: 1.01x slower                                                  |
| scimark_fft                      | 139 ms                                                                   | 141 ms: 1.01x slower                                                   |
| nbody                            | 60.1 ms                                                                  | 61.3 ms: 1.02x slower                                                  |
| xml_etree_iterparse              | 35.4 ms                                                                  | 36.4 ms: 1.03x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (31): gc_traversal, deepcopy_reduce, pylint, meteor_contest, generators, go, sphinx, sqlglot_v2_transpile, deepcopy_memo, sympy_sum, mdp, regex_effbot, sympy_integrate, nqueens, bpe_tokeniser, regex_compile, comprehensions, genshi_text, coverage, sqlite_synth, genshi_xml, k_core, pycparser, sqlglot_v2_optimize, pathlib, spectral_norm, tomli_loads, sympy_expand, sympy_str, deltablue, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x