# Results vs. 3.13.0rc2

- fork: python
- ref: bd2ed7c7ce58084c682a
- machine: darwin-arm64
- commit hash: bd2ed7c
- commit date: 2025-05-03
- overall geometric mean: 1.033x faster
- HPT reliability: 94.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 25.7 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.11x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 246 ms: 1.65x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.6 ms: 2.99x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.1 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.89 ms: 1.08x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.06x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 949 ms: 1.05x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 97.7 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.3 ms: 1.00x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.11 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.05 ms: 1.02x slower                                                    |
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.11x faster                                                     |
| mdp                              | 1.06 sec                                                       | 519 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 246 ms: 1.65x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| k_core                           | 1.46 sec                                                       | 952 ms: 1.54x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 51.5 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 876 us: 1.13x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.89 ms: 1.08x faster                                                    |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 949 ms: 1.05x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.7 us: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.5 ms: 1.01x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.3 ms: 1.00x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 65.4 us: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.05 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.4 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.2 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.03x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.0 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.9 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 47.0 ms: 1.07x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.40 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.11 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.0 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.97 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 25.7 ms: 1.11x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.59 us: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.1 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| many_optionals                   | 200 us                                                         | 238 us: 1.19x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.18 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.6 ms: 2.99x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (7): sphinx, sqlite_synth, fannkuch, pathlib, pprint_pformat, genshi_xml, regex_compile
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250503-3.14.0a7+-bd2ed7c/bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 94.18% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x