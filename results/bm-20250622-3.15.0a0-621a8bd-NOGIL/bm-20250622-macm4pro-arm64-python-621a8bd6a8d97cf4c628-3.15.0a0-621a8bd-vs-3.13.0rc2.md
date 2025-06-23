# Results vs. 3.13.0rc2

- fork: python
- ref: 621a8bd6a8d97cf4c628
- machine: darwin-arm64
- commit hash: 621a8bd
- commit date: 2025-06-22
- overall geometric mean: 1.014x faster
- HPT reliability: 74.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 997 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 55.6 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 978 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.57 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 783 us: 2.61x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 485 us: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 563 ms: 1.88x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| go                               | 72.6 ms                                                        | 60.6 ms: 1.20x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.6 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 821 ns: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 997 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 978 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.98 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| thrift                           | 309 us                                                         | 329 us: 1.06x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.03 ms: 1.07x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.31 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.0 ms: 1.10x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.57 ms: 1.11x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 71.8 us: 1.11x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.7 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.89 us: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 769 ms: 1.18x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 382 ms: 1.19x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 252 us: 1.25x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.82 us: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.13 us: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.6 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 596 us: 1.45x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.65 ms: 1.54x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 67.7 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.8 ms: 2.69x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 217 ns: 5.36x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): json_dumps, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250622-3.15.0a0-621a8bd-NOGIL/bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 74.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x