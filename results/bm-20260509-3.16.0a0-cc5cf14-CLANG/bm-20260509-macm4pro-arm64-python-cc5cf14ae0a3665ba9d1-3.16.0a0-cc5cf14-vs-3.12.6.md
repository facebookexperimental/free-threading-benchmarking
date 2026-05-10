# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: darwin-arm64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.137x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 958 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.04x faster                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 302 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.51x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 306 ms: 1.50x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 326 ms: 1.47x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 124 ms: 1.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 327 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 174 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 274 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 284 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.16x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| nbody          | 54.2 ms                                                  | 46.4 ms: 1.17x faster                                                   |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.0 ms: 1.21x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.1 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 807 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 96.6 us: 1.07x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 71.1 ms: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.99 ms: 1.05x slower                                                   |
| django_template | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.17x faster                                                   |
| pylint                           | 128 ms                                                   | 56.0 ms: 2.29x faster                                                   |
| mdp                              | 1.09 sec                                                 | 516 ms: 2.12x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.2 us: 1.68x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 302 ms: 1.64x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.58x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.51x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 306 ms: 1.50x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 326 ms: 1.47x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.03 us: 1.40x faster                                                   |
| generators                       | 21.9 ms                                                  | 15.8 ms: 1.39x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 124 ms: 1.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 327 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.8 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 174 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.1 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 274 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.0 ms: 1.21x faster                                                   |
| float                            | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.1 ms: 1.21x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.4 ns: 1.20x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.1 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 284 ms: 1.19x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 807 ms: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.18x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.1 ms: 1.17x faster                                                   |
| nbody                            | 54.2 ms                                                  | 46.4 ms: 1.17x faster                                                   |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 44.9 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| hexiom                           | 3.04 ms                                                  | 2.72 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.4 us: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| sympy_integrate                  | 8.02 ms                                                  | 7.32 ms: 1.10x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.6 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 53.7 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 97.5 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| docutils                         | 1.02 sec                                                 | 958 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.6 us: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.04x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 653 ms: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 324 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                   |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.7 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                   |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.99 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 71.1 ms: 1.05x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 880 us: 1.06x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.4 ms: 1.17x slower                                                   |
| many_optionals                   | 195 us                                                   | 232 us: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.16x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (2): bench_thread_pool, pidigits
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.137x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x