# Results vs. 3.12.6

- fork: python
- ref: f8f8c30ed4e20208e8ba
- machine: darwin-arm64
- commit hash: f8f8c30
- commit date: 2026-09-08
- overall geometric mean: 1.009x faster
- HPT reliability: 75.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 463 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 308 ms: 1.61x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 311 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 306 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 317 ms: 1.45x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.23x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 149 ms: 1.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 300 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 306 ms: 1.09x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 53.4 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 167 ms: 1.48x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 61.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.24x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.0 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 69.7 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.1 ms: 1.25x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 39.9 ms: 1.03x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 120 us: 1.16x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.4 ms: 1.17x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 166 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.31x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 6.16 ms: 1.29x slower                                                   |
| django_template | 13.6 ms                                                  | 18.1 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.31x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.63 ms: 4.48x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.59x faster                                                    |
| pylint                           | 128 ms                                                   | 54.8 ms: 2.34x faster                                                   |
| mdp                              | 1.09 sec                                                 | 631 ms: 1.73x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 489 us: 1.70x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 308 ms: 1.61x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 311 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 306 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 317 ms: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 123 us: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.1 ms: 1.25x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.24x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.23x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 149 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.6 us: 1.15x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 300 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.12x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 16.3 us: 1.12x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.91 us: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 306 ms: 1.09x faster                                                    |
| float                            | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.0 ms: 1.07x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.5 ms: 1.05x faster                                                   |
| go                               | 70.0 ms                                                  | 66.8 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 137 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| pyflate                          | 216 ms                                                   | 211 ms: 1.02x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| raytrace                         | 145 ms                                                   | 148 ms: 1.02x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 39.9 ms: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| scimark_sor                      | 61.0 ms                                                  | 63.0 ms: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 45.1 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.68 us: 1.04x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 53.3 ns: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.98 us: 1.06x slower                                                   |
| chaos                            | 28.9 ms                                                  | 30.8 ms: 1.06x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.55 ms: 1.07x slower                                                   |
| sphinx                           | 434 ms                                                   | 463 ms: 1.07x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| fannkuch                         | 176 ms                                                   | 191 ms: 1.09x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 63.3 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.6 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.4 ms: 1.12x slower                                                   |
| thrift                           | 322 us                                                   | 362 us: 1.12x slower                                                    |
| nbody                            | 54.2 ms                                                  | 61.0 ms: 1.13x slower                                                   |
| generators                       | 21.9 ms                                                  | 24.9 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 120 us: 1.16x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 382 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 53.4 ms: 1.17x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 31.4 ms: 1.17x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.57 ms: 1.17x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 781 ms: 1.17x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 197 ms: 1.18x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.04 ms: 1.19x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 166 us: 1.19x slower                                                    |
| 2to3                             | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.13 ms: 1.20x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 30.7 ms: 1.21x slower                                                   |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 69.7 ms: 1.28x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| mako                             | 4.77 ms                                                  | 6.16 ms: 1.29x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 552 us: 1.32x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.1 ms: 1.33x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 69.7 ms: 1.36x slower                                                   |
| many_optionals                   | 195 us                                                   | 272 us: 1.39x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 167 ms: 1.48x slower                                                    |
| coverage                         | 26.9 ms                                                  | 41.5 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (2): tomli_loads, pycparser
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 75.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x