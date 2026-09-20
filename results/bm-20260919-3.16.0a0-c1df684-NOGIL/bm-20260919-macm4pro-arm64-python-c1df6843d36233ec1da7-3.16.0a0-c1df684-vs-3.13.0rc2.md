# Results vs. 3.13.0rc2

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.077x slower
- HPT reliability: 99.89%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 138 ms: 1.24x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 310 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 320 ms: 1.64x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 313 ms: 1.29x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 324 ms: 1.19x faster                                                    |
| async_generators                 | 193 ms                                                         | 168 ms: 1.15x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 314 ms: 1.07x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 205 ms: 1.11x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 148 ms: 1.12x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 165 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 263 ms: 1.17x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 13.0 ms: 1.21x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 152 ms: 1.24x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 169 ms: 1.64x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 71.7 ms: 1.66x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 121 ms: 4.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.7 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                          | 1.19x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.9 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.2 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 959 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 40.2 ms: 1.12x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 121 us: 1.22x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.7 ms: 1.25x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 166 us: 1.28x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.4 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.54 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.24x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 6.07 ms: 1.37x slower                                                   |
| django_template | 12.5 ms                                                        | 18.2 ms: 1.45x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 801 us: 2.55x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 497 us: 2.00x faster                                                    |
| pylint                           | 106 ms                                                         | 54.3 ms: 1.94x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 310 ms: 1.68x faster                                                    |
| mdp                              | 1.06 sec                                                       | 637 ms: 1.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 320 ms: 1.64x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.44x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.69 ms: 1.33x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 313 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 324 ms: 1.19x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 815 ns: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| async_generators                 | 193 ms                                                         | 168 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                   |
| go                               | 72.6 ms                                                        | 67.6 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| pyflate                          | 222 ms                                                         | 212 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 959 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 62.4 ms: 1.03x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 16.2 us: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.9 ms: 1.01x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 20.0 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.13 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 314 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 505 ms: 1.07x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 205 ms: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.11x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 148 ms: 1.12x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 40.2 ms: 1.12x slower                                                   |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.13x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.56 ms: 1.14x slower                                                   |
| async_tree_none                  | 142 ms                                                         | 165 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 263 ms: 1.17x slower                                                    |
| thrift                           | 309 us                                                         | 362 us: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                   |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 386 ms: 1.20x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.4 ms: 1.20x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.69 us: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.0 ms: 1.21x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 45.1 ms: 1.21x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 36.2 ms: 1.21x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.96 us: 1.21x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 116 ms: 1.21x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.5 ms: 1.21x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 121 us: 1.22x slower                                                    |
| richards                         | 22.1 ms                                                        | 27.0 ms: 1.22x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 800 ms: 1.23x slower                                                    |
| 2to3                             | 112 ms                                                         | 138 ms: 1.24x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 198 ms: 1.24x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 30.7 ms: 1.24x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 152 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.7 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 51.0 ns: 1.26x slower                                                   |
| chaos                            | 24.3 ms                                                        | 30.7 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.54 ms: 1.27x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.63 ms: 1.27x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 166 us: 1.28x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.90 us: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.3 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| raytrace                         | 109 ms                                                         | 148 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 565 us: 1.37x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.07 ms: 1.37x slower                                                   |
| many_optionals                   | 200 us                                                         | 275 us: 1.37x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.04 ms: 1.40x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 69.2 ms: 1.44x slower                                                   |
| django_template                  | 12.5 ms                                                        | 18.2 ms: 1.45x slower                                                   |
| nbody                            | 42.5 ms                                                        | 62.7 ms: 1.47x slower                                                   |
| generators                       | 15.7 ms                                                        | 25.7 ms: 1.64x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 169 ms: 1.64x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 71.7 ms: 1.66x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 71.9 ms: 1.68x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 121 ms: 4.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (3): pathlib, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260919-3.16.0a0-c1df684-NOGIL/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.89% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.27x