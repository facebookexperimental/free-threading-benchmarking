# Results vs. 3.12.6

- fork: python
- ref: acab53212d89b298ba0d
- machine: darwin-arm64
- commit hash: acab532
- commit date: 2026-11-10
- overall geometric mean: 1.063x faster
- HPT reliability: 85.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 127 ms: 1.11x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| sphinx         | 434 ms                                                   | 452 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                    | 1.04x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 303 ms: 1.64x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 303 ms: 1.58x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 303 ms: 1.51x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 300 ms: 1.49x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 183 ms: 1.26x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.24x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 143 ms: 1.20x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 186 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 300 ms: 1.11x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.00x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.0 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 272 ms: 1.28x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 115 ms: 3.58x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.7 ms: 1.12x faster                                                       |
| pidigits       | 161 ms                                                   | 150 ms: 1.08x faster                                                        |
| nbody          | 54.2 ms                                                  | 58.7 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 64.2 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.1 ms: 1.26x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                       |
| tomli_loads          | 957 ms                                                   | 877 ms: 1.09x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.1 ms: 1.02x faster                                                       |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.5 ms: 1.10x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 159 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 7.02 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                       |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.30 ms: 4.83x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 805 us: 2.50x faster                                                        |
| pylint                           | 128 ms                                                   | 53.4 ms: 2.40x faster                                                       |
| mdp                              | 1.09 sec                                                 | 582 ms: 1.87x faster                                                        |
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 475 us: 1.75x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 303 ms: 1.64x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 303 ms: 1.58x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 303 ms: 1.51x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 300 ms: 1.49x faster                                                        |
| deepcopy                         | 161 us                                                   | 110 us: 1.46x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.8 us: 1.32x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 183 ms: 1.26x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.1 ms: 1.26x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.24x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 14.9 us: 1.23x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.21 us: 1.20x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 143 ms: 1.20x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 186 ms: 1.20x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.19x faster                                                      |
| comprehensions                   | 9.84 us                                                  | 8.30 us: 1.19x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                       |
| go                               | 70.0 ms                                                  | 60.4 ms: 1.16x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                       |
| float                            | 37.9 ms                                                  | 33.7 ms: 1.12x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                       |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.11x faster                                                      |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 300 ms: 1.11x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.3 ms: 1.10x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 877 ms: 1.09x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                       |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                        |
| pidigits                         | 161 ms                                                   | 150 ms: 1.08x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                        |
| raytrace                         | 145 ms                                                   | 137 ms: 1.06x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.46 us: 1.04x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 58.6 ms: 1.04x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 38.1 ms: 1.02x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.00x slower                                                        |
| nqueens                          | 43.5 ms                                                  | 43.8 ms: 1.01x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| sympy_integrate                  | 8.02 ms                                                  | 8.16 ms: 1.02x slower                                                       |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                       |
| sphinx                           | 434 ms                                                   | 452 ms: 1.04x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.80 ms: 1.04x slower                                                       |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                       |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 41.8 ms: 1.05x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 41.0 ms: 1.05x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.1 ms: 1.06x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.07x slower                                                        |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                       |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                        |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                        |
| nbody                            | 54.2 ms                                                  | 58.7 ms: 1.08x slower                                                       |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.9 ms: 1.09x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.8 ms: 1.10x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 50.0 ms: 1.10x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 730 ms: 1.10x slower                                                        |
| xml_etree_process                | 26.7 ms                                                  | 29.5 ms: 1.10x slower                                                       |
| 2to3                             | 114 ms                                                   | 127 ms: 1.11x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 470 us: 1.12x slower                                                        |
| shortest_path                    | 219 ms                                                   | 247 ms: 1.13x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 54.2 ms: 1.13x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 159 us: 1.14x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 64.2 ms: 1.18x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                       |
| connected_components             | 201 ms                                                   | 239 ms: 1.19x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 7.02 ms: 1.23x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 272 ms: 1.28x slower                                                        |
| many_optionals                   | 195 us                                                   | 255 us: 1.30x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 68.1 ms: 1.33x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.39x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.6 ms: 1.55x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 115 ms: 3.58x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (3): logging_silent, pycparser, html5lib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261110-3.16.0a2+dev-acab532-NOGIL/bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 85.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x