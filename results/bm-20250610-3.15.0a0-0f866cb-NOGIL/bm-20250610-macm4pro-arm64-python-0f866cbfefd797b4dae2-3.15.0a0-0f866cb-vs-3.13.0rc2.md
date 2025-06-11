# Results vs. 3.13.0rc2

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: darwin-arm64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.020x faster
- HPT reliability: 62.64%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.13 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.38 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.85 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 776 us: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 489 us: 2.03x faster                                                    |
| mdp                              | 1.06 sec                                                       | 564 ms: 1.88x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 984 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.4 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.13 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.90 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| thrift                           | 309 us                                                         | 328 us: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.06 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.38 ms: 1.09x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.3 ms: 1.11x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.0 us: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.7 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.85 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.9 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.90 us: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 376 ms: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 764 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 130 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.78 us: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.9 ms: 1.25x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.09 us: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 596 us: 1.45x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 62.1 ms: 1.45x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.58 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.68x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 217 ns: 5.34x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (4): pathlib, pycparser, html5lib, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 62.64% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x