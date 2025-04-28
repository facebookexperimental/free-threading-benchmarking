# Results vs. base

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: b739ec5
- commit date: 2025-04-28
- overall geometric mean: 1.001x faster
- HPT reliability: 98.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 124 ms                                                                   | 123 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager                 | 51.4 ms                                                                  | 50.2 ms: 1.02x faster                                    |
| async_tree_eager_io_tg           | 200 ms                                                                   | 197 ms: 1.02x faster                                     |
| async_tree_eager_memoization     | 113 ms                                                                   | 111 ms: 1.01x faster                                     |
| async_tree_eager_tg              | 79.1 ms                                                                  | 78.3 ms: 1.01x faster                                    |
| async_tree_eager_io              | 209 ms                                                                   | 207 ms: 1.01x faster                                     |
| async_generators                 | 180 ms                                                                   | 178 ms: 1.01x faster                                     |
| async_tree_eager_cpu_io_mixed    | 227 ms                                                                   | 226 ms: 1.01x faster                                     |
| async_tree_io                    | 212 ms                                                                   | 211 ms: 1.01x faster                                     |
| async_tree_none                  | 103 ms                                                                   | 102 ms: 1.01x faster                                     |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 245 ms: 1.01x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 229 ms                                                                   | 228 ms: 1.01x faster                                     |
| async_tree_memoization           | 132 ms                                                                   | 131 ms: 1.00x faster                                     |
| async_tree_cpu_io_mixed_tg       | 237 ms                                                                   | 236 ms: 1.00x faster                                     |
| async_tree_eager_memoization_tg  | 114 ms                                                                   | 113 ms: 1.00x faster                                     |
| async_tree_memoization_tg        | 125 ms                                                                   | 124 ms: 1.00x faster                                     |
| async_tree_io_tg                 | 198 ms                                                                   | 198 ms: 1.00x faster                                     |
| coroutines                       | 10.0 ms                                                                  | 10.3 ms: 1.02x slower                                    |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 167 ms                                                                   | 167 ms: 1.00x slower                                     |
| nbody          | 56.3 ms                                                                  | 56.9 ms: 1.01x slower                                    |
| Geometric mean | (ref)                                                                    | 1.00x slower                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 1.55 ms                                                                  | 1.51 ms: 1.03x faster                                    |
| regex_compile  | 53.2 ms                                                                  | 53.3 ms: 1.00x slower                                    |
| regex_dna      | 101 ms                                                                   | 102 ms: 1.00x slower                                     |
| Geometric mean | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|--------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse    | 60.9 ms                                                                  | 58.6 ms: 1.04x faster                                    |
| pickle_pure_python | 154 us                                                                   | 152 us: 1.01x faster                                     |
| json_dumps         | 5.22 ms                                                                  | 5.17 ms: 1.01x faster                                    |
| tomli_loads        | 1.01 sec                                                                 | 1000 ms: 1.01x faster                                    |
| json_loads         | 12.5 us                                                                  | 12.4 us: 1.01x faster                                    |
| xml_etree_process  | 26.9 ms                                                                  | 26.8 ms: 1.00x faster                                    |
| Geometric mean     | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 9.55 ms                                                                  | 9.61 ms: 1.01x slower                                    |
| python_startup_no_site | 6.91 ms                                                                  | 6.96 ms: 1.01x slower                                    |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                             |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_text, genshi_xml, mako

All benchmarks:
===============

| Benchmark                        | bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7+-58567cc | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse                  | 60.9 ms                                                                  | 58.6 ms: 1.04x faster                                    |
| regex_effbot                     | 1.55 ms                                                                  | 1.51 ms: 1.03x faster                                    |
| spectral_norm                    | 51.5 ms                                                                  | 50.3 ms: 1.02x faster                                    |
| async_tree_eager                 | 51.4 ms                                                                  | 50.2 ms: 1.02x faster                                    |
| telco                            | 3.35 ms                                                                  | 3.29 ms: 1.02x faster                                    |
| async_tree_eager_io_tg           | 200 ms                                                                   | 197 ms: 1.02x faster                                     |
| json                             | 2.05 ms                                                                  | 2.02 ms: 1.01x faster                                    |
| logging_silent                   | 45.2 ns                                                                  | 44.6 ns: 1.01x faster                                    |
| async_tree_eager_memoization     | 113 ms                                                                   | 111 ms: 1.01x faster                                     |
| coverage                         | 40.3 ms                                                                  | 39.9 ms: 1.01x faster                                    |
| pickle_pure_python               | 154 us                                                                   | 152 us: 1.01x faster                                     |
| deepcopy_reduce                  | 1.29 us                                                                  | 1.28 us: 1.01x faster                                    |
| crypto_pyaes                     | 42.8 ms                                                                  | 42.4 ms: 1.01x faster                                    |
| async_tree_eager_tg              | 79.1 ms                                                                  | 78.3 ms: 1.01x faster                                    |
| async_tree_eager_io              | 209 ms                                                                   | 207 ms: 1.01x faster                                     |
| async_generators                 | 180 ms                                                                   | 178 ms: 1.01x faster                                     |
| sympy_sum                        | 62.9 ms                                                                  | 62.3 ms: 1.01x faster                                    |
| json_dumps                       | 5.22 ms                                                                  | 5.17 ms: 1.01x faster                                    |
| tomli_loads                      | 1.01 sec                                                                 | 1000 ms: 1.01x faster                                    |
| raytrace                         | 131 ms                                                                   | 130 ms: 1.01x faster                                     |
| richards_super                   | 28.0 ms                                                                  | 27.8 ms: 1.01x faster                                    |
| json_loads                       | 12.5 us                                                                  | 12.4 us: 1.01x faster                                    |
| 2to3                             | 124 ms                                                                   | 123 ms: 1.01x faster                                     |
| subparsers                       | 9.03 ms                                                                  | 8.97 ms: 1.01x faster                                    |
| nqueens                          | 42.0 ms                                                                  | 41.7 ms: 1.01x faster                                    |
| async_tree_eager_cpu_io_mixed    | 227 ms                                                                   | 226 ms: 1.01x faster                                     |
| async_tree_io                    | 212 ms                                                                   | 211 ms: 1.01x faster                                     |
| mdp                              | 585 ms                                                                   | 582 ms: 1.01x faster                                     |
| sqlglot_v2_normalize             | 49.3 ms                                                                  | 49.0 ms: 1.01x faster                                    |
| async_tree_none                  | 103 ms                                                                   | 102 ms: 1.01x faster                                     |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 245 ms: 1.01x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 229 ms                                                                   | 228 ms: 1.01x faster                                     |
| sympy_expand                     | 192 ms                                                                   | 191 ms: 1.01x faster                                     |
| many_optionals                   | 250 us                                                                   | 249 us: 1.00x faster                                     |
| async_tree_memoization           | 132 ms                                                                   | 131 ms: 1.00x faster                                     |
| sqlglot_v2_transpile             | 738 us                                                                   | 735 us: 1.00x faster                                     |
| sqlglot_v2_parse                 | 606 us                                                                   | 604 us: 1.00x faster                                     |
| generators                       | 19.1 ms                                                                  | 19.0 ms: 1.00x faster                                    |
| richards                         | 24.6 ms                                                                  | 24.5 ms: 1.00x faster                                    |
| async_tree_cpu_io_mixed_tg       | 237 ms                                                                   | 236 ms: 1.00x faster                                     |
| async_tree_eager_memoization_tg  | 114 ms                                                                   | 113 ms: 1.00x faster                                     |
| xml_etree_process                | 26.9 ms                                                                  | 26.8 ms: 1.00x faster                                    |
| async_tree_memoization_tg        | 125 ms                                                                   | 124 ms: 1.00x faster                                     |
| async_tree_io_tg                 | 198 ms                                                                   | 198 ms: 1.00x faster                                     |
| comprehensions                   | 8.77 us                                                                  | 8.78 us: 1.00x slower                                    |
| bpe_tokeniser                    | 1.98 sec                                                                 | 1.98 sec: 1.00x slower                                   |
| pylint                           | 114 ms                                                                   | 115 ms: 1.00x slower                                     |
| sqlalchemy_declarative           | 51.3 ms                                                                  | 51.4 ms: 1.00x slower                                    |
| regex_compile                    | 53.2 ms                                                                  | 53.3 ms: 1.00x slower                                    |
| sympy_str                        | 112 ms                                                                   | 112 ms: 1.00x slower                                     |
| fannkuch                         | 191 ms                                                                   | 192 ms: 1.00x slower                                     |
| regex_dna                        | 101 ms                                                                   | 102 ms: 1.00x slower                                     |
| pidigits                         | 167 ms                                                                   | 167 ms: 1.00x slower                                     |
| sqlalchemy_imperative            | 5.94 ms                                                                  | 5.97 ms: 1.01x slower                                    |
| go                               | 63.0 ms                                                                  | 63.3 ms: 1.01x slower                                    |
| shortest_path                    | 232 ms                                                                   | 233 ms: 1.01x slower                                     |
| python_startup                   | 9.55 ms                                                                  | 9.61 ms: 1.01x slower                                    |
| python_startup_no_site           | 6.91 ms                                                                  | 6.96 ms: 1.01x slower                                    |
| logging_format                   | 2.90 us                                                                  | 2.93 us: 1.01x slower                                    |
| scimark_lu                       | 54.2 ms                                                                  | 54.7 ms: 1.01x slower                                    |
| hexiom                           | 3.22 ms                                                                  | 3.24 ms: 1.01x slower                                    |
| scimark_sor                      | 54.7 ms                                                                  | 55.2 ms: 1.01x slower                                    |
| meteor_contest                   | 57.4 ms                                                                  | 58.0 ms: 1.01x slower                                    |
| logging_simple                   | 2.63 us                                                                  | 2.66 us: 1.01x slower                                    |
| nbody                            | 56.3 ms                                                                  | 56.9 ms: 1.01x slower                                    |
| scimark_monte_carlo              | 33.1 ms                                                                  | 33.5 ms: 1.01x slower                                    |
| pprint_safe_repr                 | 356 ms                                                                   | 363 ms: 1.02x slower                                     |
| coroutines                       | 10.0 ms                                                                  | 10.3 ms: 1.02x slower                                    |
| pprint_pformat                   | 725 ms                                                                   | 743 ms: 1.03x slower                                     |
| scimark_fft                      | 143 ms                                                                   | 147 ms: 1.03x slower                                     |
| scimark_sparse_mat_mult          | 2.12 ms                                                                  | 2.18 ms: 1.03x slower                                    |
| pyflate                          | 202 ms                                                                   | 209 ms: 1.03x slower                                     |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (31): xml_etree_iterparse, k_core, deltablue, create_gc_cycles, typing_runtime_protocols, sqlite_synth, float, deepcopy, pathlib, regex_v8, docutils, sympy_integrate, bench_mp_pool, asyncio_websockets, xml_etree_generate, django_template, async_tree_none_tg, sphinx, genshi_text, pycparser, html5lib, unpickle_pure_python, dulwich_log, genshi_xml, mako, chaos, sqlglot_v2_optimize, bench_thread_pool, connected_components, deepcopy_memo, gc_traversal

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 98.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x