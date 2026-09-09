# Results vs. 3.13.0rc2

- fork: python
- ref: f8f8c30ed4e20208e8ba
- machine: darwin-arm64
- commit hash: f8f8c30
- commit date: 2026-09-08
- overall geometric mean: 1.066x slower
- HPT reliability: 99.81%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 137 ms: 1.22x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.06x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 463 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 308 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 306 ms: 1.70x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 311 ms: 1.30x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 317 ms: 1.22x faster                                                    |
| async_generators                 | 193 ms                                                         | 167 ms: 1.15x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 306 ms: 1.04x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 53.4 ms: 1.24x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.9 ms: 1.29x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 167 ms: 1.63x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 61.0 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.7 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.4 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 953 ms: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.9 ms: 1.12x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 120 us: 1.20x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 166 us: 1.28x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 6.16 ms: 1.40x slower                                                   |
| django_template | 12.5 ms                                                        | 18.1 ms: 1.45x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.42x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 777 us: 2.63x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 489 us: 2.03x faster                                                    |
| pylint                           | 106 ms                                                         | 54.8 ms: 1.93x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 308 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 306 ms: 1.70x faster                                                    |
| mdp                              | 1.06 sec                                                       | 631 ms: 1.68x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.63 ms: 1.35x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 311 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 317 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| deepcopy                         | 145 us                                                         | 123 us: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| async_generators                 | 193 ms                                                         | 167 ms: 1.15x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.4 ms: 1.09x faster                                                   |
| go                               | 72.6 ms                                                        | 66.8 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| pyflate                          | 222 ms                                                         | 211 ms: 1.05x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 953 ms: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.6 us: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 63.0 ms: 1.02x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 16.3 us: 1.01x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.9 ms: 1.01x slower                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.30 us: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.13 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 306 ms: 1.04x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.06x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 191 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.9 ms: 1.12x slower                                                   |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 463 ms: 1.13x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.55 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| shortest_path                    | 225 ms                                                         | 256 ms: 1.14x slower                                                    |
| thrift                           | 309 us                                                         | 362 us: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                   |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 382 ms: 1.19x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.6 ms: 1.19x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.68 us: 1.20x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 781 ms: 1.20x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 120 us: 1.20x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.21x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 45.1 ms: 1.21x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 63.3 ms: 1.21x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.98 us: 1.22x slower                                                   |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| 2to3                             | 112 ms                                                         | 137 ms: 1.22x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 197 ms: 1.23x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 53.4 ms: 1.24x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.7 ms: 1.24x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.57 ms: 1.25x slower                                                   |
| chaos                            | 24.3 ms                                                        | 30.8 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 166 us: 1.28x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 13.9 ms: 1.29x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.91 us: 1.31x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 53.3 ns: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.5 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 552 us: 1.34x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                    |
| raytrace                         | 109 ms                                                         | 148 ms: 1.36x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.16 ms: 1.40x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.04 ms: 1.41x slower                                                   |
| nbody                            | 42.5 ms                                                        | 61.0 ms: 1.44x slower                                                   |
| django_template                  | 12.5 ms                                                        | 18.1 ms: 1.45x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 69.7 ms: 1.45x slower                                                   |
| generators                       | 15.7 ms                                                        | 24.9 ms: 1.59x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 167 ms: 1.63x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 69.7 ms: 1.63x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 99.81% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.27x