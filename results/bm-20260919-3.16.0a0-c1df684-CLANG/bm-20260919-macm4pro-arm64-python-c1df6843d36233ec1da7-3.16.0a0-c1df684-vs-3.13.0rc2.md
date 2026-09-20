# Results vs. 3.13.0rc2

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.040x faster
- HPT reliability: 90.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 952 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 344 ms: 1.53x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 344 ms: 1.52x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 329 ms: 1.23x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 341 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 251 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.8 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.63x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 44.9 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.03 ms: 1.19x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 89.0 ms: 1.06x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.62 ms: 1.28x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 806 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.4 us: 1.08x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.54 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.93 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                    |
| pylint                           | 106 ms                                                         | 56.3 ms: 1.88x faster                                                   |
| deepcopy                         | 145 us                                                         | 93.5 us: 1.55x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 344 ms: 1.53x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 344 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                   |
| go                               | 72.6 ms                                                        | 52.5 ms: 1.38x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 47.8 ms: 1.34x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 48.7 us: 1.33x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.62 ms: 1.28x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 806 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 329 ms: 1.23x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.03 ms: 1.19x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 850 us: 1.17x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 341 ms: 1.13x faster                                                    |
| docutils                         | 1.05 sec                                                       | 952 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 92.4 us: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 89.0 ms: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.68 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| richards                         | 22.1 ms                                                        | 21.0 ms: 1.05x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.5 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.64 us: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.35 ms: 1.02x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.00 ms: 1.02x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 406 us: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.2 ms: 1.01x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 319 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.00x faster                                                   |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 211 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 664 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.7 ms: 1.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                   |
| generators                       | 15.7 ms                                                        | 16.1 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.6 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.9 ms: 1.06x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.1 ms: 1.08x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.54 ms: 1.10x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 251 ms: 1.12x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.93 ms: 1.16x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.8 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.63x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (2): async_tree_memoization, json_loads
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 90.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x