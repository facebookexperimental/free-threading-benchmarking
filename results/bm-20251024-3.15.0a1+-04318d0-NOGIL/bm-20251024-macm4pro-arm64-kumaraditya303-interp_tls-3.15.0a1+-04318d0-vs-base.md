# Results vs. base

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.004x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 1.01 sec                                                                 | 1.01 sec: 1.01x slower                                                 |
| html5lib       | 23.8 ms                                                                  | 23.9 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                           |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                       | 10.8 ms                                                                  | 10.6 ms: 1.03x faster                                                  |
| asyncio_websockets               | 190 ms                                                                   | 189 ms: 1.00x faster                                                   |
| async_tree_io                    | 213 ms                                                                   | 213 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                   | 225 ms: 1.00x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 236 ms                                                                   | 237 ms: 1.00x slower                                                   |
| async_tree_eager_memoization     | 110 ms                                                                   | 111 ms: 1.00x slower                                                   |
| async_tree_memoization_tg        | 125 ms                                                                   | 125 ms: 1.00x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                                   | 113 ms: 1.01x slower                                                   |
| async_tree_eager_io              | 207 ms                                                                   | 209 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 228 ms                                                                   | 229 ms: 1.01x slower                                                   |
| async_tree_eager                 | 49.4 ms                                                                  | 49.7 ms: 1.01x slower                                                  |
| async_tree_io_tg                 | 200 ms                                                                   | 201 ms: 1.01x slower                                                   |
| async_tree_eager_tg              | 78.9 ms                                                                  | 79.5 ms: 1.01x slower                                                  |
| async_tree_none_tg               | 87.7 ms                                                                  | 88.3 ms: 1.01x slower                                                  |
| async_tree_eager_io_tg           | 196 ms                                                                   | 198 ms: 1.01x slower                                                   |
| async_generators                 | 181 ms                                                                   | 184 ms: 1.02x slower                                                   |
| Geometric mean                   | (ref)                                                                    | 1.00x slower                                                           |

Benchmark hidden because not significant (3): async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 165 ms                                                                   | 165 ms: 1.00x faster                                                   |
| float          | 29.9 ms                                                                  | 30.1 ms: 1.01x slower                                                  |
| nbody          | 58.8 ms                                                                  | 61.0 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 9.65 ms                                                                  | 9.29 ms: 1.04x faster                                                  |
| regex_effbot   | 1.45 ms                                                                  | 1.43 ms: 1.01x faster                                                  |
| regex_dna      | 95.7 ms                                                                  | 94.6 ms: 1.01x faster                                                  |
| regex_compile  | 53.4 ms                                                                  | 53.9 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 59.9 ms                                                                  | 58.7 ms: 1.02x faster                                                  |
| json_loads           | 11.6 us                                                                  | 11.5 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 38.7 ms                                                                  | 38.4 ms: 1.01x faster                                                  |
| pickle_pure_python   | 153 us                                                                   | 154 us: 1.00x slower                                                   |
| json_dumps           | 4.04 ms                                                                  | 4.07 ms: 1.01x slower                                                  |
| unpickle_pure_python | 112 us                                                                   | 112 us: 1.01x slower                                                   |
| tomli_loads          | 968 ms                                                                   | 977 ms: 1.01x slower                                                   |
| xml_etree_process    | 27.0 ms                                                                  | 27.3 ms: 1.01x slower                                                  |
| xml_etree_generate   | 36.9 ms                                                                  | 37.4 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.11 ms                                                                  | 7.08 ms: 1.00x faster                                                  |
| python_startup         | 9.75 ms                                                                  | 9.74 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 5.86 ms                                                                  | 5.81 ms: 1.01x faster                                                  |
| genshi_text    | 11.9 ms                                                                  | 12.0 ms: 1.01x slower                                                  |
| genshi_xml     | 24.8 ms                                                                  | 25.2 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8                         | 9.65 ms                                                                  | 9.29 ms: 1.04x faster                                                  |
| coroutines                       | 10.8 ms                                                                  | 10.6 ms: 1.03x faster                                                  |
| xml_etree_parse                  | 59.9 ms                                                                  | 58.7 ms: 1.02x faster                                                  |
| gc_traversal                     | 776 us                                                                   | 763 us: 1.02x faster                                                   |
| create_gc_cycles                 | 482 us                                                                   | 474 us: 1.02x faster                                                   |
| regex_effbot                     | 1.45 ms                                                                  | 1.43 ms: 1.01x faster                                                  |
| regex_dna                        | 95.7 ms                                                                  | 94.6 ms: 1.01x faster                                                  |
| json_loads                       | 11.6 us                                                                  | 11.5 us: 1.01x faster                                                  |
| mako                             | 5.86 ms                                                                  | 5.81 ms: 1.01x faster                                                  |
| xml_etree_iterparse              | 38.7 ms                                                                  | 38.4 ms: 1.01x faster                                                  |
| python_startup_no_site           | 7.11 ms                                                                  | 7.08 ms: 1.00x faster                                                  |
| asyncio_websockets               | 190 ms                                                                   | 189 ms: 1.00x faster                                                   |
| bench_mp_pool                    | 42.8 ms                                                                  | 42.7 ms: 1.00x faster                                                  |
| pidigits                         | 165 ms                                                                   | 165 ms: 1.00x faster                                                   |
| comprehensions                   | 8.54 us                                                                  | 8.51 us: 1.00x faster                                                  |
| python_startup                   | 9.75 ms                                                                  | 9.74 ms: 1.00x faster                                                  |
| async_tree_io                    | 213 ms                                                                   | 213 ms: 1.00x slower                                                   |
| connected_components             | 222 ms                                                                   | 223 ms: 1.00x slower                                                   |
| sympy_integrate                  | 8.05 ms                                                                  | 8.09 ms: 1.00x slower                                                  |
| sqlglot_v2_optimize              | 24.6 ms                                                                  | 24.7 ms: 1.00x slower                                                  |
| pickle_pure_python               | 153 us                                                                   | 154 us: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                   | 225 ms: 1.00x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 236 ms                                                                   | 237 ms: 1.00x slower                                                   |
| async_tree_eager_memoization     | 110 ms                                                                   | 111 ms: 1.00x slower                                                   |
| async_tree_memoization_tg        | 125 ms                                                                   | 125 ms: 1.00x slower                                                   |
| fannkuch                         | 186 ms                                                                   | 187 ms: 1.01x slower                                                   |
| scimark_lu                       | 56.7 ms                                                                  | 56.9 ms: 1.01x slower                                                  |
| meteor_contest                   | 56.6 ms                                                                  | 56.9 ms: 1.01x slower                                                  |
| docutils                         | 1.01 sec                                                                 | 1.01 sec: 1.01x slower                                                 |
| sqlglot_v2_normalize             | 49.9 ms                                                                  | 50.2 ms: 1.01x slower                                                  |
| many_optionals                   | 391 us                                                                   | 393 us: 1.01x slower                                                   |
| json_dumps                       | 4.04 ms                                                                  | 4.07 ms: 1.01x slower                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                                   | 113 ms: 1.01x slower                                                   |
| richards                         | 24.1 ms                                                                  | 24.2 ms: 1.01x slower                                                  |
| async_tree_eager_io              | 207 ms                                                                   | 209 ms: 1.01x slower                                                   |
| html5lib                         | 23.8 ms                                                                  | 23.9 ms: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 228 ms                                                                   | 229 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 112 us                                                                   | 112 us: 1.01x slower                                                   |
| async_tree_eager                 | 49.4 ms                                                                  | 49.7 ms: 1.01x slower                                                  |
| async_tree_io_tg                 | 200 ms                                                                   | 201 ms: 1.01x slower                                                   |
| async_tree_eager_tg              | 78.9 ms                                                                  | 79.5 ms: 1.01x slower                                                  |
| bench_thread_pool                | 544 us                                                                   | 548 us: 1.01x slower                                                   |
| genshi_text                      | 11.9 ms                                                                  | 12.0 ms: 1.01x slower                                                  |
| async_tree_none_tg               | 87.7 ms                                                                  | 88.3 ms: 1.01x slower                                                  |
| async_tree_eager_io_tg           | 196 ms                                                                   | 198 ms: 1.01x slower                                                   |
| float                            | 29.9 ms                                                                  | 30.1 ms: 1.01x slower                                                  |
| regex_compile                    | 53.4 ms                                                                  | 53.9 ms: 1.01x slower                                                  |
| sympy_expand                     | 191 ms                                                                   | 193 ms: 1.01x slower                                                   |
| tomli_loads                      | 968 ms                                                                   | 977 ms: 1.01x slower                                                   |
| xml_etree_process                | 27.0 ms                                                                  | 27.3 ms: 1.01x slower                                                  |
| deepcopy_reduce                  | 1.27 us                                                                  | 1.29 us: 1.01x slower                                                  |
| go                               | 62.5 ms                                                                  | 63.2 ms: 1.01x slower                                                  |
| logging_simple                   | 2.52 us                                                                  | 2.55 us: 1.01x slower                                                  |
| logging_format                   | 2.80 us                                                                  | 2.83 us: 1.01x slower                                                  |
| crypto_pyaes                     | 42.5 ms                                                                  | 43.0 ms: 1.01x slower                                                  |
| xml_etree_generate               | 36.9 ms                                                                  | 37.4 ms: 1.01x slower                                                  |
| generators                       | 19.2 ms                                                                  | 19.4 ms: 1.01x slower                                                  |
| logging_silent                   | 45.4 ns                                                                  | 46.0 ns: 1.01x slower                                                  |
| mdp                              | 611 ms                                                                   | 619 ms: 1.01x slower                                                   |
| nqueens                          | 44.0 ms                                                                  | 44.6 ms: 1.01x slower                                                  |
| sympy_str                        | 111 ms                                                                   | 113 ms: 1.01x slower                                                   |
| thrift                           | 339 us                                                                   | 344 us: 1.01x slower                                                   |
| pycparser                        | 471 ms                                                                   | 477 ms: 1.01x slower                                                   |
| spectral_norm                    | 50.4 ms                                                                  | 51.1 ms: 1.01x slower                                                  |
| telco                            | 3.03 ms                                                                  | 3.08 ms: 1.01x slower                                                  |
| bpe_tokeniser                    | 2.00 sec                                                                 | 2.03 sec: 1.02x slower                                                 |
| deepcopy                         | 118 us                                                                   | 120 us: 1.02x slower                                                   |
| async_generators                 | 181 ms                                                                   | 184 ms: 1.02x slower                                                   |
| hexiom                           | 3.20 ms                                                                  | 3.25 ms: 1.02x slower                                                  |
| scimark_monte_carlo              | 33.6 ms                                                                  | 34.2 ms: 1.02x slower                                                  |
| genshi_xml                       | 24.8 ms                                                                  | 25.2 ms: 1.02x slower                                                  |
| coverage                         | 40.1 ms                                                                  | 40.9 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult          | 2.20 ms                                                                  | 2.25 ms: 1.02x slower                                                  |
| scimark_sor                      | 55.3 ms                                                                  | 56.6 ms: 1.02x slower                                                  |
| deepcopy_memo                    | 13.2 us                                                                  | 13.6 us: 1.03x slower                                                  |
| nbody                            | 58.8 ms                                                                  | 61.0 ms: 1.04x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.00x slower                                                           |

Benchmark hidden because not significant (27): sqlglot_v2_transpile, pyflate, pylint, sqlite_synth, django_template, sqlglot_v2_parse, async_tree_none, scimark_fft, pathlib, json, 2to3, richards_super, dask, dulwich_log, k_core, async_tree_cpu_io_mixed, async_tree_memoization, pprint_pformat, pprint_safe_repr, typing_runtime_protocols, chaos, shortest_path, sympy_sum, raytrace, subparsers, deltablue, sphinx

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x