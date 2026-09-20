# Results vs. 3.12.6

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.239x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 942 ms: 1.09x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 397 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 305 ms: 1.57x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 321 ms: 1.54x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 115 ms: 1.49x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 124 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 319 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 166 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.84 ms: 1.38x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.35x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 173 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 277 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 131 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 246 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 60.7 ms: 1.33x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 98.3 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 32.1 ms: 1.69x faster                                                   |
| float          | 37.9 ms                                                  | 23.3 ms: 1.63x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.37 ms: 1.22x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 46.9 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 108 us: 1.29x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.32 ms: 1.28x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 80.9 us: 1.27x faster                                                   |
| tomli_loads          | 957 ms                                                   | 767 ms: 1.25x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 22.8 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 33.6 ms: 1.16x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.8 ms: 1.03x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.19x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.32 ms: 1.16x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.80 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.87 ms: 1.23x faster                                                   |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.74 ms: 5.56x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 10.9 ms: 2.32x faster                                                   |
| richards                         | 22.4 ms                                                  | 9.73 ms: 2.30x faster                                                   |
| pylint                           | 128 ms                                                   | 56.0 ms: 2.29x faster                                                   |
| mdp                              | 1.09 sec                                                 | 573 ms: 1.91x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 32.5 ms: 1.88x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 32.1 ms: 1.69x faster                                                   |
| nbody                            | 54.2 ms                                                  | 32.1 ms: 1.69x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 10.8 us: 1.69x faster                                                   |
| deepcopy                         | 161 us                                                   | 96.5 us: 1.67x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 5.89 us: 1.67x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 31.3 ms: 1.64x faster                                                   |
| float                            | 37.9 ms                                                  | 23.3 ms: 1.63x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 44.3 us: 1.60x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 305 ms: 1.57x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 321 ms: 1.54x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 115 ms: 1.49x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 96.1 ms: 1.48x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 992 ns: 1.47x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 1.75 us: 1.47x faster                                                   |
| logging_format                   | 2.80 us                                                  | 1.92 us: 1.46x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.19 ms: 1.45x faster                                                   |
| raytrace                         | 145 ms                                                   | 100.0 ms: 1.45x faster                                                  |
| go                               | 70.0 ms                                                  | 48.5 ms: 1.44x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 124 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 319 ms: 1.44x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 30.3 ms: 1.43x faster                                                   |
| chaos                            | 28.9 ms                                                  | 20.4 ms: 1.42x faster                                                   |
| pyflate                          | 216 ms                                                   | 154 ms: 1.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 319 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 166 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.84 ms: 1.38x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.35x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 24.4 ms: 1.32x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 252 ms: 1.30x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 514 ms: 1.29x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 108 us: 1.29x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 173 ms: 1.29x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.32 ms: 1.28x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 80.9 us: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.41 ms: 1.26x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 767 ms: 1.25x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 31.4 ms: 1.24x faster                                                   |
| mako                             | 4.77 ms                                                  | 3.87 ms: 1.23x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.3 ms: 1.23x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.69 ms: 1.23x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.37 ms: 1.22x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.85 sec: 1.21x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 42.2 ns: 1.21x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 277 ms: 1.20x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 22.8 ms: 1.17x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 46.9 ms: 1.16x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 33.6 ms: 1.16x faster                                                   |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.15x faster                                                    |
| sphinx                           | 434 ms                                                   | 397 ms: 1.09x faster                                                    |
| docutils                         | 1.02 sec                                                 | 942 ms: 1.09x faster                                                    |
| sympy_str                        | 104 ms                                                   | 96.2 ms: 1.08x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 53.3 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 160 ms: 1.04x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 45.9 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 931 ns: 1.04x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.8 ms: 1.03x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.99 ms: 1.01x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 131 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.13 sec: 1.01x slower                                                  |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 425 us: 1.02x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 848 us: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 246 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.32 ms: 1.16x slower                                                   |
| many_optionals                   | 195 us                                                   | 232 us: 1.19x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.80 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 60.7 ms: 1.33x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 98.3 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmark hidden because not significant (3): pycparser, telco, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.239x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.26x