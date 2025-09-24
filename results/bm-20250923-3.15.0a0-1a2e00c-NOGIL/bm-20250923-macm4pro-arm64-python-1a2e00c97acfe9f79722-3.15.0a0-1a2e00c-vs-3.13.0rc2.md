# Results vs. 3.13.0rc2

- fork: python
- ref: 1a2e00c97acfe9f79722
- machine: darwin-arm64
- commit hash: 1a2e00c
- commit date: 2025-09-23
- overall geometric mean: 1.024x faster
- HPT reliability: 62.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 966 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.63x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 84.3 ms: 1.57x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.53x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 97.6 ms: 1.46x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 237 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.8 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.1 ms: 2.63x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.27x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                    |
| nbody          | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.4 ms: 1.11x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 949 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.91 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 745 us: 2.74x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.63x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 466 us: 2.13x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                    |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 84.3 ms: 1.57x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 97.6 ms: 1.46x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                                   |
| deepcopy                         | 145 us                                                         | 114 us: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 237 ms: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 60.9 ms: 1.19x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 813 ns: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                   |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 56.4 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 966 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 949 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.93 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.08x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 708 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.50 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 47.8 ms: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.48 us: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.8 us: 1.14x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 59.8 ms: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.91 ms: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.17x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.6 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.9 ms: 1.19x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.22 us: 1.21x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.3 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 590 us: 1.43x slower                                                    |
| many_optionals                   | 200 us                                                         | 326 us: 1.62x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.1 ms: 2.63x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (3): json, coroutines, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250923-3.15.0a0-1a2e00c-NOGIL/bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 62.80% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x