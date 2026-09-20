# Results vs. 3.12.6

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.129x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 947 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.41 ms: 1.44x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 345 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 344 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.33x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 344 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 285 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 292 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 134 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 248 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.1 ms: 1.43x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| nbody          | 54.2 ms                                                  | 42.7 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.5 ms: 1.19x faster                                                   |
| tomli_loads          | 957 ms                                                   | 818 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.4 us: 1.05x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.13 ms: 5.03x faster                                                   |
| pylint                           | 128 ms                                                   | 56.2 ms: 2.28x faster                                                   |
| mdp                              | 1.09 sec                                                 | 511 ms: 2.14x faster                                                    |
| deepcopy                         | 161 us                                                   | 95.6 us: 1.69x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.62 us: 1.49x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.0 us: 1.45x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.41 ms: 1.44x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 345 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 344 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.7 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 344 ms: 1.30x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.27x faster                                                   |
| nbody                            | 54.2 ms                                                  | 42.7 ms: 1.27x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.8 ms: 1.27x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 34.8 ms: 1.25x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.25x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| raytrace                         | 145 ms                                                   | 120 ms: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.5 ms: 1.19x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 285 ms: 1.17x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 818 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.17x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 292 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| k_core                           | 1.12 sec                                                 | 980 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.3 ms: 1.14x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.68 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.10x faster                                                   |
| fannkuch                         | 176 ms                                                   | 159 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.10x faster                                                   |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| docutils                         | 1.02 sec                                                 | 947 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 923 ns: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.4 us: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.6 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.04x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.7 ms: 1.03x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 319 ms: 1.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 486 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.1 ms: 1.02x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 658 ms: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 420 us: 1.00x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 837 us: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 134 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                   |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 248 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.1 ms: 1.43x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, regex_compile
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.129x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.22x