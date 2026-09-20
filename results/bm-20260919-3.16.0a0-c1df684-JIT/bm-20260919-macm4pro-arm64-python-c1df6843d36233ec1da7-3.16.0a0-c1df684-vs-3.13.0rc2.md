# Results vs. 3.13.0rc2

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.145x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 942 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                   |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 321 ms: 1.64x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 319 ms: 1.63x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 305 ms: 1.33x faster                                                    |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 115 ms: 1.15x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 166 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 277 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 131 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 246 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 264 ms: 1.27x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 60.7 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 98.3 ms: 3.40x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                   |
| nbody          | 42.5 ms                                                        | 32.1 ms: 1.33x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.21x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.37 ms: 1.18x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.5 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.9 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.32 ms: 1.40x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 767 ms: 1.30x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 80.9 us: 1.23x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 108 us: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 22.8 ms: 1.11x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.6 ms: 1.06x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.8 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.32 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.87 ms: 1.14x faster                                                   |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                         | 22.1 ms                                                        | 9.73 ms: 2.27x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 10.9 ms: 2.26x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 32.5 ms: 1.97x faster                                                   |
| pylint                           | 106 ms                                                         | 56.0 ms: 1.89x faster                                                   |
| mdp                              | 1.06 sec                                                       | 573 ms: 1.85x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 3.74 ms: 1.68x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 321 ms: 1.64x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 319 ms: 1.63x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.8 us: 1.52x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.5 us: 1.50x faster                                                   |
| go                               | 72.6 ms                                                        | 48.5 ms: 1.50x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 44.3 us: 1.46x faster                                                   |
| pyflate                          | 222 ms                                                         | 154 ms: 1.44x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.32 ms: 1.40x faster                                                   |
| scimark_lu                       | 42.8 ms                                                        | 31.3 ms: 1.37x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 32.1 ms: 1.36x faster                                                   |
| float                            | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 305 ms: 1.33x faster                                                    |
| nbody                            | 42.5 ms                                                        | 32.1 ms: 1.33x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 992 ns: 1.31x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 767 ms: 1.30x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.13 sec: 1.29x faster                                                  |
| scimark_fft                      | 124 ms                                                         | 96.1 ms: 1.29x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 1.75 us: 1.28x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 252 ms: 1.28x faster                                                    |
| logging_format                   | 2.45 us                                                        | 1.92 us: 1.27x faster                                                   |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 514 ms: 1.26x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 80.9 us: 1.23x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 30.3 ms: 1.23x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 24.4 ms: 1.23x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.19 ms: 1.22x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| pickle_pure_python               | 130 us                                                         | 108 us: 1.20x faster                                                    |
| chaos                            | 24.3 ms                                                        | 20.4 ms: 1.19x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.41 ms: 1.18x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.60 ms: 1.18x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.37 ms: 1.18x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 848 us: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 5.89 us: 1.16x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.85 sec: 1.15x faster                                                  |
| async_tree_none_tg               | 133 ms                                                         | 115 ms: 1.15x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.3 ms: 1.15x faster                                                   |
| mako                             | 4.41 ms                                                        | 3.87 ms: 1.14x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 166 ms: 1.12x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 22.8 ms: 1.11x faster                                                   |
| docutils                         | 1.05 sec                                                       | 942 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| raytrace                         | 109 ms                                                         | 100.0 ms: 1.09x faster                                                  |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 31.4 ms: 1.07x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 173 ms: 1.07x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 33.6 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 277 ms: 1.06x faster                                                    |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.69 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                   |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.5 ms: 1.02x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.9 ms: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 931 ns: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 160 ms: 1.00x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 96.2 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.3 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 425 us: 1.03x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 494 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.8 ms: 1.06x slower                                                   |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 131 ms: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.32 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 246 ms: 1.09x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                   |
| many_optionals                   | 200 us                                                         | 232 us: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 264 ms: 1.27x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 60.7 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 98.3 ms: 3.40x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.145x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x