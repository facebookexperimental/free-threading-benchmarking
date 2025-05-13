# Results vs. 3.13.0rc2

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: darwin-arm64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.005x slower
- HPT reliability: 87.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 26.4 ms: 1.14x slower                                                   |
| sphinx         | 409 ms                                                         | 426 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.0 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.7 ms: 1.17x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 55.4 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.9 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.37 ms: 1.15x slower                                                   |
| json_loads           | 10.8 us                                                        | 12.7 us: 1.17x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                   |
| mako            | 4.41 ms                                                        | 5.67 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 789 us: 2.59x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 493 us: 2.01x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| mdp                              | 1.06 sec                                                       | 586 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.0 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 823 ns: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| deepcopy                         | 145 us                                                         | 127 us: 1.15x faster                                                    |
| go                               | 72.6 ms                                                        | 63.7 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 481 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 231 ms: 1.03x slower                                                    |
| sphinx                           | 409 ms                                                         | 426 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                   |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                   |
| json                             | 1.94 ms                                                        | 2.10 ms: 1.08x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.39 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 359 ms: 1.12x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.9 ms: 1.13x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.9 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 26.4 ms: 1.14x slower                                                   |
| pylint                           | 106 ms                                                         | 121 ms: 1.14x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.4 ms: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.37 ms: 1.15x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.2 ms: 1.17x slower                                                   |
| json_loads                       | 10.8 us                                                        | 12.7 us: 1.17x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 50.7 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 76.2 us: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.8 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.7 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.1 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.67 ms: 1.29x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.77 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.4 ms: 1.30x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.90 us: 1.30x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.18 us: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.4 ms: 1.30x slower                                                   |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                    |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 582 us: 1.41x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 67.2 ms: 1.57x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 10.1 ms: 1.61x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 216 ns: 5.33x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, deepcopy_reduce
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 87.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x