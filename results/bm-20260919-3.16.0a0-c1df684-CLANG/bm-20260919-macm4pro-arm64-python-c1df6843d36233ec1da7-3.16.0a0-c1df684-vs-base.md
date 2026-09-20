# Results vs. base

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.002x slower
- HPT reliability: 84.72%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 120 ms                                                                                                            | 119 ms: 1.00x faster                                                                                                    |
| docutils       | 947 ms                                                                                                            | 952 ms: 1.01x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets               | 191 ms                                                                                                            | 191 ms: 1.00x slower                                                                                                    |
| async_tree_eager_memoization     | 134 ms                                                                                                            | 135 ms: 1.01x slower                                                                                                    |
| asyncio_tcp_ssl                  | 545 ms                                                                                                            | 550 ms: 1.01x slower                                                                                                    |
| async_tree_eager_tg              | 104 ms                                                                                                            | 105 ms: 1.01x slower                                                                                                    |
| asyncio_tcp                      | 160 ms                                                                                                            | 161 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 248 ms                                                                                                            | 251 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 264 ms                                                                                                            | 268 ms: 1.02x slower                                                                                                    |
| coroutines                       | 9.41 ms                                                                                                           | 10.3 ms: 1.09x slower                                                                                                   |
| async_generators                 | 145 ms                                                                                                            | 180 ms: 1.24x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (12): async_tree_io, async_tree_io_tg, async_tree_eager, async_tree_none, async_tree_eager_io, async_tree_memoization, async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 167 ms                                                                                                            | 171 ms: 1.02x slower                                                                                                    |
| float          | 28.9 ms                                                                                                           | 29.7 ms: 1.03x slower                                                                                                   |
| nbody          | 42.7 ms                                                                                                           | 44.9 ms: 1.05x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 92.3 ms                                                                                                           | 89.0 ms: 1.04x faster                                                                                                   |
| regex_v8       | 9.29 ms                                                                                                           | 9.03 ms: 1.03x faster                                                                                                   |
| regex_compile  | 54.7 ms                                                                                                           | 54.5 ms: 1.00x faster                                                                                                   |
| regex_effbot   | 1.32 ms                                                                                                           | 1.33 ms: 1.01x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 43.5 ms                                                                                                           | 40.7 ms: 1.07x faster                                                                                                   |
| unpickle_pure_python | 98.4 us                                                                                                           | 92.4 us: 1.07x faster                                                                                                   |
| xml_etree_generate   | 35.8 ms                                                                                                           | 34.2 ms: 1.05x faster                                                                                                   |
| unpickle             | 6.36 us                                                                                                           | 6.19 us: 1.03x faster                                                                                                   |
| unpickle_list        | 2.06 us                                                                                                           | 2.01 us: 1.02x faster                                                                                                   |
| xml_etree_process    | 25.2 ms                                                                                                           | 24.7 ms: 1.02x faster                                                                                                   |
| tomli_loads          | 818 ms                                                                                                            | 806 ms: 1.01x faster                                                                                                    |
| xml_etree_parse      | 66.6 ms                                                                                                           | 65.7 ms: 1.01x faster                                                                                                   |
| pickle_pure_python   | 140 us                                                                                                            | 139 us: 1.01x faster                                                                                                    |
| json_loads           | 10.7 us                                                                                                           | 10.8 us: 1.01x slower                                                                                                   |
| json_dumps           | 3.57 ms                                                                                                           | 3.62 ms: 1.01x slower                                                                                                   |
| pickle_list          | 2.32 us                                                                                                           | 2.35 us: 1.01x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.71 ms                                                                                                           | 6.93 ms: 1.03x slower                                                                                                   |
| python_startup         | 9.20 ms                                                                                                           | 9.54 ms: 1.04x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 14.9 ms                                                                                                           | 14.7 ms: 1.01x faster                                                                                                   |
| mako            | 4.62 ms                                                                                                           | 4.85 ms: 1.05x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.02x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                        | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| scimark_lu                       | 49.7 ms                                                                                                           | 46.1 ms: 1.08x faster                                                                                                   |
| generators                       | 17.2 ms                                                                                                           | 16.1 ms: 1.07x faster                                                                                                   |
| xml_etree_iterparse              | 43.5 ms                                                                                                           | 40.7 ms: 1.07x faster                                                                                                   |
| unpickle_pure_python             | 98.4 us                                                                                                           | 92.4 us: 1.07x faster                                                                                                   |
| raytrace                         | 120 ms                                                                                                            | 115 ms: 1.05x faster                                                                                                    |
| xml_etree_generate               | 35.8 ms                                                                                                           | 34.2 ms: 1.05x faster                                                                                                   |
| scimark_sparse_mat_mult          | 1.85 ms                                                                                                           | 1.77 ms: 1.04x faster                                                                                                   |
| regex_dna                        | 92.3 ms                                                                                                           | 89.0 ms: 1.04x faster                                                                                                   |
| bench_thread_pool                | 420 us                                                                                                            | 406 us: 1.03x faster                                                                                                    |
| regex_v8                         | 9.29 ms                                                                                                           | 9.03 ms: 1.03x faster                                                                                                   |
| sqlglot_v2_normalize             | 45.4 ms                                                                                                           | 44.2 ms: 1.03x faster                                                                                                   |
| pyflate                          | 190 ms                                                                                                            | 185 ms: 1.03x faster                                                                                                    |
| unpickle                         | 6.36 us                                                                                                           | 6.19 us: 1.03x faster                                                                                                   |
| unpack_sequence                  | 23.4 ns                                                                                                           | 22.8 ns: 1.03x faster                                                                                                   |
| scimark_sor                      | 49.0 ms                                                                                                           | 47.8 ms: 1.02x faster                                                                                                   |
| sqlglot_v2_optimize              | 22.2 ms                                                                                                           | 21.7 ms: 1.02x faster                                                                                                   |
| telco                            | 2.88 ms                                                                                                           | 2.82 ms: 1.02x faster                                                                                                   |
| deepcopy                         | 95.6 us                                                                                                           | 93.5 us: 1.02x faster                                                                                                   |
| scimark_monte_carlo              | 28.3 ms                                                                                                           | 27.7 ms: 1.02x faster                                                                                                   |
| unpickle_list                    | 2.06 us                                                                                                           | 2.01 us: 1.02x faster                                                                                                   |
| crypto_pyaes                     | 38.1 ms                                                                                                           | 37.3 ms: 1.02x faster                                                                                                   |
| sympy_expand                     | 169 ms                                                                                                            | 166 ms: 1.02x faster                                                                                                    |
| sqlglot_v2_transpile             | 618 us                                                                                                            | 606 us: 1.02x faster                                                                                                    |
| sympy_str                        | 99.6 ms                                                                                                           | 97.7 ms: 1.02x faster                                                                                                   |
| xml_etree_process                | 25.2 ms                                                                                                           | 24.7 ms: 1.02x faster                                                                                                   |
| sqlglot_v2_parse                 | 502 us                                                                                                            | 494 us: 1.02x faster                                                                                                    |
| django_template                  | 14.9 ms                                                                                                           | 14.7 ms: 1.01x faster                                                                                                   |
| tomli_loads                      | 818 ms                                                                                                            | 806 ms: 1.01x faster                                                                                                    |
| sympy_sum                        | 55.3 ms                                                                                                           | 54.6 ms: 1.01x faster                                                                                                   |
| xml_etree_parse                  | 66.6 ms                                                                                                           | 65.7 ms: 1.01x faster                                                                                                   |
| sympy_integrate                  | 7.44 ms                                                                                                           | 7.35 ms: 1.01x faster                                                                                                   |
| thrift                           | 311 us                                                                                                            | 307 us: 1.01x faster                                                                                                    |
| pickle_pure_python               | 140 us                                                                                                            | 139 us: 1.01x faster                                                                                                    |
| deepcopy_reduce                  | 1.03 us                                                                                                           | 1.02 us: 1.01x faster                                                                                                   |
| many_optionals                   | 245 us                                                                                                            | 243 us: 1.01x faster                                                                                                    |
| subparsers                       | 4.13 ms                                                                                                           | 4.11 ms: 1.01x faster                                                                                                   |
| go                               | 52.7 ms                                                                                                           | 52.5 ms: 1.00x faster                                                                                                   |
| regex_compile                    | 54.7 ms                                                                                                           | 54.5 ms: 1.00x faster                                                                                                   |
| 2to3                             | 120 ms                                                                                                            | 119 ms: 1.00x faster                                                                                                    |
| asyncio_websockets               | 191 ms                                                                                                            | 191 ms: 1.00x slower                                                                                                    |
| deepcopy_memo                    | 11.8 us                                                                                                           | 11.8 us: 1.00x slower                                                                                                   |
| async_tree_eager_memoization     | 134 ms                                                                                                            | 135 ms: 1.01x slower                                                                                                    |
| docutils                         | 947 ms                                                                                                            | 952 ms: 1.01x slower                                                                                                    |
| dulwich_log                      | 18.2 ms                                                                                                           | 18.3 ms: 1.01x slower                                                                                                   |
| regex_effbot                     | 1.32 ms                                                                                                           | 1.33 ms: 1.01x slower                                                                                                   |
| meteor_contest                   | 48.8 ms                                                                                                           | 49.2 ms: 1.01x slower                                                                                                   |
| chaos                            | 25.5 ms                                                                                                           | 25.8 ms: 1.01x slower                                                                                                   |
| spectral_norm                    | 42.8 ms                                                                                                           | 43.2 ms: 1.01x slower                                                                                                   |
| deltablue                        | 1.48 ms                                                                                                           | 1.49 ms: 1.01x slower                                                                                                   |
| logging_simple                   | 2.17 us                                                                                                           | 2.19 us: 1.01x slower                                                                                                   |
| pprint_pformat                   | 658 ms                                                                                                            | 664 ms: 1.01x slower                                                                                                    |
| asyncio_tcp_ssl                  | 545 ms                                                                                                            | 550 ms: 1.01x slower                                                                                                    |
| async_tree_eager_tg              | 104 ms                                                                                                            | 105 ms: 1.01x slower                                                                                                    |
| asyncio_tcp                      | 160 ms                                                                                                            | 161 ms: 1.01x slower                                                                                                    |
| json_loads                       | 10.7 us                                                                                                           | 10.8 us: 1.01x slower                                                                                                   |
| sqlite_synth                     | 923 ns                                                                                                            | 935 ns: 1.01x slower                                                                                                    |
| shortest_path                    | 224 ms                                                                                                            | 227 ms: 1.01x slower                                                                                                    |
| pycparser                        | 486 ms                                                                                                            | 493 ms: 1.01x slower                                                                                                    |
| mdp                              | 511 ms                                                                                                            | 518 ms: 1.01x slower                                                                                                    |
| json_dumps                       | 3.57 ms                                                                                                           | 3.62 ms: 1.01x slower                                                                                                   |
| pickle_list                      | 2.32 us                                                                                                           | 2.35 us: 1.01x slower                                                                                                   |
| async_tree_eager_cpu_io_mixed    | 248 ms                                                                                                            | 251 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 264 ms                                                                                                            | 268 ms: 1.02x slower                                                                                                    |
| create_gc_cycles                 | 837 us                                                                                                            | 850 us: 1.02x slower                                                                                                    |
| connected_components             | 207 ms                                                                                                            | 211 ms: 1.02x slower                                                                                                    |
| gc_traversal                     | 1.96 ms                                                                                                           | 2.00 ms: 1.02x slower                                                                                                   |
| nqueens                          | 34.8 ms                                                                                                           | 35.5 ms: 1.02x slower                                                                                                   |
| pidigits                         | 167 ms                                                                                                            | 171 ms: 1.02x slower                                                                                                    |
| richards_super                   | 23.2 ms                                                                                                           | 23.8 ms: 1.03x slower                                                                                                   |
| float                            | 28.9 ms                                                                                                           | 29.7 ms: 1.03x slower                                                                                                   |
| bpe_tokeniser                    | 1.95 sec                                                                                                          | 2.01 sec: 1.03x slower                                                                                                  |
| python_startup_no_site           | 6.71 ms                                                                                                           | 6.93 ms: 1.03x slower                                                                                                   |
| richards                         | 20.3 ms                                                                                                           | 21.0 ms: 1.03x slower                                                                                                   |
| python_startup                   | 9.20 ms                                                                                                           | 9.54 ms: 1.04x slower                                                                                                   |
| mako                             | 4.62 ms                                                                                                           | 4.85 ms: 1.05x slower                                                                                                   |
| nbody                            | 42.7 ms                                                                                                           | 44.9 ms: 1.05x slower                                                                                                   |
| coroutines                       | 9.41 ms                                                                                                           | 10.3 ms: 1.09x slower                                                                                                   |
| fannkuch                         | 159 ms                                                                                                            | 183 ms: 1.14x slower                                                                                                    |
| async_generators                 | 145 ms                                                                                                            | 180 ms: 1.24x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                             | 1.00x slower                                                                                                            |

Benchmark hidden because not significant (28): html5lib, async_tree_io, async_tree_io_tg, typing_runtime_protocols, async_tree_eager, async_tree_none, logging_format, async_tree_eager_io, async_tree_memoization, scimark_fft, async_tree_eager_io_tg, pickle, pickle_dict, hexiom, bench_mp_pool, pprint_safe_repr, pathlib, pylint, async_tree_memoization_tg, comprehensions, sphinx, async_tree_none_tg, async_tree_cpu_io_mixed, json, async_tree_cpu_io_mixed_tg, logging_silent, async_tree_eager_memoization_tg, k_core

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 84.72% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x