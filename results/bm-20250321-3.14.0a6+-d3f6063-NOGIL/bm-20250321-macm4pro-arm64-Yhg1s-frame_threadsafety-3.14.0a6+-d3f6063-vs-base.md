# Results vs. base

- fork: Yhg1s
- ref: frame_threadsafety
- machine: darwin-arm64
- commit hash: d3f6063
- commit date: 2025-03-21
- overall geometric mean: 1.004x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 132 ms                                                                   | 130 ms: 1.01x faster                                                  |
| docutils       | 1.05 sec                                                                 | 1.04 sec: 1.00x faster                                                |
| sphinx         | 439 ms                                                                   | 442 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                       | 12.5 ms                                                                  | 12.2 ms: 1.02x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 230 ms                                                                   | 227 ms: 1.01x faster                                                  |
| async_tree_eager                 | 56.6 ms                                                                  | 56.0 ms: 1.01x faster                                                 |
| async_tree_io_tg                 | 226 ms                                                                   | 223 ms: 1.01x faster                                                  |
| async_tree_none_tg               | 100 ms                                                                   | 99.2 ms: 1.01x faster                                                 |
| async_tree_none                  | 116 ms                                                                   | 115 ms: 1.01x faster                                                  |
| async_tree_eager_tg              | 88.3 ms                                                                  | 87.5 ms: 1.01x faster                                                 |
| async_tree_eager_cpu_io_mixed_tg | 233 ms                                                                   | 231 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed          | 254 ms                                                                   | 252 ms: 1.01x faster                                                  |
| async_generators                 | 192 ms                                                                   | 191 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 243 ms                                                                   | 242 ms: 1.01x faster                                                  |
| async_tree_io                    | 241 ms                                                                   | 239 ms: 1.01x faster                                                  |
| asyncio_websockets               | 189 ms                                                                   | 188 ms: 1.01x faster                                                  |
| async_tree_eager_io_tg           | 223 ms                                                                   | 222 ms: 1.01x faster                                                  |
| async_tree_eager_io              | 233 ms                                                                   | 232 ms: 1.00x faster                                                  |
| async_tree_eager_memoization     | 121 ms                                                                   | 120 ms: 1.00x faster                                                  |
| async_tree_eager_memoization_tg  | 123 ms                                                                   | 123 ms: 1.00x faster                                                  |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 36.3 ms                                                                  | 35.8 ms: 1.01x faster                                                 |
| nbody          | 78.7 ms                                                                  | 77.7 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 100 ms                                                                   | 98.5 ms: 1.02x faster                                                 |
| regex_compile  | 59.5 ms                                                                  | 59.4 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 57.3 ms                                                                  | 56.2 ms: 1.02x faster                                                 |
| json_dumps           | 5.26 ms                                                                  | 5.19 ms: 1.01x faster                                                 |
| unpickle_pure_python | 128 us                                                                   | 127 us: 1.01x faster                                                  |
| xml_etree_generate   | 41.3 ms                                                                  | 41.1 ms: 1.00x faster                                                 |
| pickle_pure_python   | 170 us                                                                   | 171 us: 1.00x slower                                                  |
| xml_etree_iterparse  | 39.7 ms                                                                  | 40.2 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                          |

Benchmark hidden because not significant (3): json_loads, xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.22 ms                                                                  | 9.23 ms: 1.00x slower                                                 |
| python_startup_no_site | 7.27 ms                                                                  | 7.28 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                    | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 6.25 ms                                                                  | 6.21 ms: 1.01x faster                                                 |
| genshi_text    | 13.2 ms                                                                  | 13.1 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                          |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pyflate                          | 239 ms                                                                   | 232 ms: 1.03x faster                                                  |
| fannkuch                         | 227 ms                                                                   | 221 ms: 1.03x faster                                                  |
| coroutines                       | 12.5 ms                                                                  | 12.2 ms: 1.02x faster                                                 |
| logging_silent                   | 56.2 ns                                                                  | 55.1 ns: 1.02x faster                                                 |
| xml_etree_parse                  | 57.3 ms                                                                  | 56.2 ms: 1.02x faster                                                 |
| richards                         | 28.0 ms                                                                  | 27.6 ms: 1.02x faster                                                 |
| regex_dna                        | 100 ms                                                                   | 98.5 ms: 1.02x faster                                                 |
| many_optionals                   | 254 us                                                                   | 250 us: 1.02x faster                                                  |
| float                            | 36.3 ms                                                                  | 35.8 ms: 1.01x faster                                                 |
| meteor_contest                   | 60.5 ms                                                                  | 59.6 ms: 1.01x faster                                                 |
| deepcopy_memo                    | 17.3 us                                                                  | 17.1 us: 1.01x faster                                                 |
| json_dumps                       | 5.26 ms                                                                  | 5.19 ms: 1.01x faster                                                 |
| nbody                            | 78.7 ms                                                                  | 77.7 ms: 1.01x faster                                                 |
| scimark_fft                      | 164 ms                                                                   | 162 ms: 1.01x faster                                                  |
| 2to3                             | 132 ms                                                                   | 130 ms: 1.01x faster                                                  |
| dulwich_log                      | 19.8 ms                                                                  | 19.6 ms: 1.01x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 230 ms                                                                   | 227 ms: 1.01x faster                                                  |
| json                             | 2.01 ms                                                                  | 1.99 ms: 1.01x faster                                                 |
| async_tree_eager                 | 56.6 ms                                                                  | 56.0 ms: 1.01x faster                                                 |
| async_tree_io_tg                 | 226 ms                                                                   | 223 ms: 1.01x faster                                                  |
| unpickle_pure_python             | 128 us                                                                   | 127 us: 1.01x faster                                                  |
| async_tree_none_tg               | 100 ms                                                                   | 99.2 ms: 1.01x faster                                                 |
| go                               | 74.8 ms                                                                  | 74.1 ms: 1.01x faster                                                 |
| nqueens                          | 49.7 ms                                                                  | 49.3 ms: 1.01x faster                                                 |
| async_tree_none                  | 116 ms                                                                   | 115 ms: 1.01x faster                                                  |
| async_tree_eager_tg              | 88.3 ms                                                                  | 87.5 ms: 1.01x faster                                                 |
| async_tree_eager_cpu_io_mixed_tg | 233 ms                                                                   | 231 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed          | 254 ms                                                                   | 252 ms: 1.01x faster                                                  |
| deltablue                        | 2.00 ms                                                                  | 1.98 ms: 1.01x faster                                                 |
| async_generators                 | 192 ms                                                                   | 191 ms: 1.01x faster                                                  |
| hexiom                           | 3.99 ms                                                                  | 3.96 ms: 1.01x faster                                                 |
| deepcopy                         | 129 us                                                                   | 128 us: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 243 ms                                                                   | 242 ms: 1.01x faster                                                  |
| bench_mp_pool                    | 40.2 ms                                                                  | 39.9 ms: 1.01x faster                                                 |
| async_tree_io                    | 241 ms                                                                   | 239 ms: 1.01x faster                                                  |
| asyncio_websockets               | 189 ms                                                                   | 188 ms: 1.01x faster                                                  |
| crypto_pyaes                     | 46.3 ms                                                                  | 45.9 ms: 1.01x faster                                                 |
| async_tree_eager_io_tg           | 223 ms                                                                   | 222 ms: 1.01x faster                                                  |
| sqlite_synth                     | 845 ns                                                                   | 840 ns: 1.01x faster                                                  |
| subparsers                       | 9.41 ms                                                                  | 9.35 ms: 1.01x faster                                                 |
| mako                             | 6.25 ms                                                                  | 6.21 ms: 1.01x faster                                                 |
| telco                            | 3.62 ms                                                                  | 3.60 ms: 1.01x faster                                                 |
| sqlglot_v2_normalize             | 53.5 ms                                                                  | 53.3 ms: 1.01x faster                                                 |
| genshi_text                      | 13.2 ms                                                                  | 13.1 ms: 1.00x faster                                                 |
| async_tree_eager_io              | 233 ms                                                                   | 232 ms: 1.00x faster                                                  |
| comprehensions                   | 10.1 us                                                                  | 10.1 us: 1.00x faster                                                 |
| async_tree_eager_memoization     | 121 ms                                                                   | 120 ms: 1.00x faster                                                  |
| sqlglot_v2_optimize              | 26.4 ms                                                                  | 26.3 ms: 1.00x faster                                                 |
| xml_etree_generate               | 41.3 ms                                                                  | 41.1 ms: 1.00x faster                                                 |
| regex_compile                    | 59.5 ms                                                                  | 59.4 ms: 1.00x faster                                                 |
| async_tree_eager_memoization_tg  | 123 ms                                                                   | 123 ms: 1.00x faster                                                  |
| scimark_sparse_mat_mult          | 2.52 ms                                                                  | 2.52 ms: 1.00x faster                                                 |
| pprint_safe_repr                 | 415 ms                                                                   | 414 ms: 1.00x faster                                                  |
| docutils                         | 1.05 sec                                                                 | 1.04 sec: 1.00x faster                                                |
| python_startup                   | 9.22 ms                                                                  | 9.23 ms: 1.00x slower                                                 |
| python_startup_no_site           | 7.27 ms                                                                  | 7.28 ms: 1.00x slower                                                 |
| connected_components             | 235 ms                                                                   | 236 ms: 1.00x slower                                                  |
| sqlglot_v2_parse                 | 701 us                                                                   | 703 us: 1.00x slower                                                  |
| sqlalchemy_declarative           | 51.3 ms                                                                  | 51.5 ms: 1.00x slower                                                 |
| pickle_pure_python               | 170 us                                                                   | 171 us: 1.00x slower                                                  |
| spectral_norm                    | 59.2 ms                                                                  | 59.5 ms: 1.00x slower                                                 |
| logging_format                   | 3.14 us                                                                  | 3.15 us: 1.00x slower                                                 |
| thrift                           | 348 us                                                                   | 350 us: 1.00x slower                                                  |
| mdp                              | 1.19 sec                                                                 | 1.19 sec: 1.00x slower                                                |
| scimark_sor                      | 69.7 ms                                                                  | 70.1 ms: 1.01x slower                                                 |
| sphinx                           | 439 ms                                                                   | 442 ms: 1.01x slower                                                  |
| generators                       | 22.3 ms                                                                  | 22.5 ms: 1.01x slower                                                 |
| scimark_lu                       | 67.3 ms                                                                  | 67.8 ms: 1.01x slower                                                 |
| raytrace                         | 161 ms                                                                   | 162 ms: 1.01x slower                                                  |
| sympy_expand                     | 203 ms                                                                   | 204 ms: 1.01x slower                                                  |
| sympy_str                        | 119 ms                                                                   | 120 ms: 1.01x slower                                                  |
| sqlalchemy_imperative            | 5.90 ms                                                                  | 5.95 ms: 1.01x slower                                                 |
| sympy_integrate                  | 9.05 ms                                                                  | 9.13 ms: 1.01x slower                                                 |
| gc_traversal                     | 925 us                                                                   | 935 us: 1.01x slower                                                  |
| xml_etree_iterparse              | 39.7 ms                                                                  | 40.2 ms: 1.01x slower                                                 |
| bench_thread_pool                | 625 us                                                                   | 634 us: 1.01x slower                                                  |
| create_gc_cycles                 | 502 us                                                                   | 510 us: 1.02x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                          |

Benchmark hidden because not significant (27): typing_runtime_protocols, deepcopy_reduce, json_loads, pidigits, async_tree_memoization_tg, xml_etree_process, async_tree_memoization, django_template, pprint_pformat, pycparser, html5lib, chaos, shortest_path, bpe_tokeniser, regex_v8, tomli_loads, pathlib, pylint, scimark_monte_carlo, richards_super, coverage, regex_effbot, sqlglot_v2_transpile, genshi_xml, sympy_sum, logging_simple, k_core

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x