# Results vs. 3.12.6

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.126x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 952 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 344 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.36x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 341 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 344 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 251 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.8 ms: 1.42x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 44.9 ms: 1.21x faster                                                   |
| pidigits       | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 89.0 ms: 1.12x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.03 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                   |
| tomli_loads          | 957 ms                                                   | 806 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.62 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 92.4 us: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.7 ms: 1.03x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 139 us: 1.00x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.54 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.93 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                   |
| pylint                           | 128 ms                                                   | 56.3 ms: 2.28x faster                                                   |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                    |
| deepcopy                         | 161 us                                                   | 93.5 us: 1.73x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.64 us: 1.48x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.7 us: 1.46x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 344 ms: 1.44x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.36x faster                                                    |
| generators                       | 21.9 ms                                                  | 16.1 ms: 1.36x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 341 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.5 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 344 ms: 1.30x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 47.8 ms: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                   |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.2 ms: 1.26x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 35.5 ms: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.9 ms: 1.21x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 806 ms: 1.19x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.62 ms: 1.18x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.18x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                   |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.68 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 89.0 ms: 1.12x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 92.4 us: 1.11x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.1 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                  |
| sympy_integrate                  | 8.02 ms                                                  | 7.35 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                   |
| docutils                         | 1.02 sec                                                 | 952 ms: 1.07x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.0 ms: 1.07x faster                                                   |
| sympy_str                        | 104 ms                                                   | 97.7 ms: 1.07x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.07x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.03 ms: 1.06x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.6 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 935 ns: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.7 ms: 1.03x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 406 us: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 319 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| pycparser                        | 497 ms                                                   | 493 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.00 ms: 1.01x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 139 us: 1.00x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.02x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 850 us: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                   |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                    |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                    |
| pidigits                         | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 251 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.54 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.93 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 243 us: 1.24x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.8 ms: 1.42x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (3): json_loads, regex_compile, pprint_pformat
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260919-3.16.0a0-c1df684-CLANG/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x