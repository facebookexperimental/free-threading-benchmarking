# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: darwin-arm64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.050x faster
- HPT reliability: 98.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 958 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 327 ms: 1.59x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 306 ms: 1.26x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 326 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 284 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 174 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 257 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.51x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 46.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 45.0 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.71 ms: 1.25x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 807 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.1 ms: 1.07x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 71.1 ms: 1.14x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.99 ms: 1.13x slower                                                   |
| django_template | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 516 ms: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 56.0 ms: 1.88x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 327 ms: 1.59x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.2 us: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                   |
| go                               | 72.6 ms                                                        | 52.8 ms: 1.37x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 306 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.71 ms: 1.25x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 326 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 807 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 880 us: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 958 ms: 1.09x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.1 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.07x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 45.0 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 284 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 174 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.6 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.32 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                    |
| generators                       | 15.7 ms                                                        | 15.8 ms: 1.00x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 653 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 324 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 418 us: 1.02x slower                                                    |
| connected_components             | 208 ms                                                         | 211 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.5 ms: 1.02x slower                                                   |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.7 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.1 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.03 us: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.4 ns: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 44.9 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 46.4 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.99 ms: 1.13x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 71.1 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                   |
| many_optionals                   | 200 us                                                         | 232 us: 1.16x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 39.7 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.4 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 257 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.51x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (5): sphinx, nqueens, typing_runtime_protocols, float, dask
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 98.93% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x