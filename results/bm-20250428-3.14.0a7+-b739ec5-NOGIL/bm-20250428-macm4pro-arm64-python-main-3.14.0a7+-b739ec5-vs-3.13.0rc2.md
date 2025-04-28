# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: b739ec5
- commit date: 2025-04-28
- overall geometric mean: 1.003x faster
- HPT reliability: 92.19%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                   |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                    |
| sphinx         | 409 ms                                                         | 428 ms: 1.05x slower                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.40x faster                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                     |
| nbody          | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                    |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                    |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                     |
| regex_compile  | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.6 ms: 1.06x faster                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                     |
| json_dumps           | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                    |
| json_loads           | 10.8 us                                                        | 12.4 us: 1.15x slower                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                     |
| Geometric mean       | (ref)                                                          | 1.04x slower                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                    |
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                    |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                     |
| create_gc_cycles                 | 993 us                                                         | 453 us: 2.19x faster                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                     |
| mdp                              | 1.06 sec                                                       | 582 ms: 1.82x faster                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.9 ms: 1.53x faster                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                     |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.40x faster                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.2 ms: 1.16x faster                                    |
| deepcopy                         | 145 us                                                         | 126 us: 1.16x faster                                     |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                     |
| go                               | 72.6 ms                                                        | 63.3 ms: 1.15x faster                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.6 us: 1.13x faster                                    |
| float                            | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                     |
| regex_v8                         | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.6 ms: 1.06x faster                                    |
| pyflate                          | 222 ms                                                         | 209 ms: 1.06x faster                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                     |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                    |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                     |
| json                             | 1.94 ms                                                        | 2.02 ms: 1.04x slower                                    |
| sphinx                           | 409 ms                                                         | 428 ms: 1.05x slower                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                    |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                     |
| fannkuch                         | 179 ms                                                         | 192 ms: 1.07x slower                                     |
| telco                            | 3.07 ms                                                        | 3.29 ms: 1.07x slower                                    |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.20 ms: 1.09x slower                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                     |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                     |
| richards                         | 22.1 ms                                                        | 24.5 ms: 1.11x slower                                    |
| regex_compile                    | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                    |
| json_dumps                       | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                    |
| python_startup                   | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                    |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                    |
| richards_super                   | 24.7 ms                                                        | 27.8 ms: 1.13x slower                                    |
| pprint_safe_repr                 | 322 ms                                                         | 363 ms: 1.13x slower                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                    |
| hexiom                           | 2.85 ms                                                        | 3.24 ms: 1.14x slower                                    |
| pprint_pformat                   | 650 ms                                                         | 743 ms: 1.14x slower                                     |
| json_loads                       | 10.8 us                                                        | 12.4 us: 1.15x slower                                    |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.3 us: 1.15x slower                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.4 ms: 1.16x slower                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.18x slower                                     |
| scimark_fft                      | 124 ms                                                         | 147 ms: 1.19x slower                                     |
| logging_simple                   | 2.24 us                                                        | 2.66 us: 1.19x slower                                    |
| sympy_sum                        | 52.3 ms                                                        | 62.3 ms: 1.19x slower                                    |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.97 ms: 1.19x slower                                    |
| logging_format                   | 2.45 us                                                        | 2.93 us: 1.20x slower                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                     |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                    |
| meteor_contest                   | 47.9 ms                                                        | 58.0 ms: 1.21x slower                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                     |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                    |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.7 ms: 1.28x slower                                    |
| comprehensions                   | 6.80 us                                                        | 8.78 us: 1.29x slower                                    |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                    |
| nbody                            | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                    |
| subparsers                       | 6.26 ms                                                        | 8.97 ms: 1.43x slower                                    |
| bench_thread_pool                | 412 us                                                         | 598 us: 1.45x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                             |

Benchmark hidden because not significant (1): tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250428-3.14.0a7+-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 92.19% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x