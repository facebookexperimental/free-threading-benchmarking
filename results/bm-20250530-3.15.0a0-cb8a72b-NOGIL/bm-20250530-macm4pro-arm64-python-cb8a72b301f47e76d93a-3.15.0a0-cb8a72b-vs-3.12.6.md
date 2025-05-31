# Results vs. 3.12.6

- fork: python
- ref: cb8a72b301f47e76d93a
- machine: darwin-arm64
- commit hash: cb8a72b
- commit date: 2025-05-30
- overall geometric mean: 1.096x faster
- HPT reliability: 98.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 989 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.6 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.1 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.0 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.0 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 991 ms: 1.04x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.51 ms: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| json_loads           | 10.9 us                                                  | 12.3 us: 1.14x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.41 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.86 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.66 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 761 us: 2.64x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.63 ms: 2.16x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.6 ms: 1.99x faster                                                   |
| mdp                              | 1.09 sec                                                 | 562 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 481 us: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.89 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 819 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.17x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.0 ms: 1.07x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.4 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 989 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.03 ms: 1.00x faster                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.0 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 991 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.7 us: 1.04x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.2 ms: 1.05x slower                                                   |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.06x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.51 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.1 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.82 us: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.10 us: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.2 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.3 us: 1.14x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 381 ms: 1.16x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 778 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.41 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.66 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.86 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.30 ms: 1.26x slower                                                   |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 68.3 ms: 1.33x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 596 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.0 ms: 2.40x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 215 ns: 4.23x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250530-3.15.0a0-cb8a72b-NOGIL/bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 98.44% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x