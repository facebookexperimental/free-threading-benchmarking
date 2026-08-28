# Results vs. 3.13.0rc2

- fork: python
- ref: 24e5a55ccb0c5db68136
- machine: darwin-arm64
- commit hash: 24e5a55
- commit date: 2026-08-27
- overall geometric mean: 1.055x slower
- HPT reliability: 99.39%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 134 ms: 1.20x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.08 sec: 1.04x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 458 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 308 ms: 1.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 311 ms: 1.69x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 311 ms: 1.30x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 316 ms: 1.22x faster                                                    |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 146 ms: 1.03x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 190 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 304 ms: 1.03x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 127 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 236 ms: 1.05x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 145 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 51.8 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.6 ms: 1.27x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 158 ms: 1.55x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 118 ms: 4.09x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 35.0 ms: 1.11x slower                                                   |
| nbody          | 42.5 ms                                                        | 63.1 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 68.1 ms: 1.42x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.4 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 938 ms: 1.07x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 39.2 ms: 1.09x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 118 us: 1.18x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.3 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 164 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.50 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 17.8 ms: 1.42x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.37x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 770 us: 2.65x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 54.3 ms: 1.94x faster                                                   |
| mdp                              | 1.06 sec                                                       | 617 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 308 ms: 1.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 311 ms: 1.69x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.52 ms: 1.39x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 311 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                   |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 316 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 805 ns: 1.18x faster                                                    |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                                   |
| go                               | 72.6 ms                                                        | 66.1 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.4 ms: 1.09x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.1 us: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 59.9 us: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 938 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| pyflate                          | 222 ms                                                         | 212 ms: 1.05x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 61.3 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.01x slower                                                   |
| async_tree_none                  | 142 ms                                                         | 146 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| async_tree_memoization           | 184 ms                                                         | 190 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 304 ms: 1.03x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.08 sec: 1.04x slower                                                  |
| async_tree_eager_memoization     | 122 ms                                                         | 127 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 236 ms: 1.05x slower                                                    |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 504 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.09x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.2 ms: 1.09x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 145 ms: 1.09x slower                                                    |
| float                            | 31.4 ms                                                        | 35.0 ms: 1.11x slower                                                   |
| sphinx                           | 409 ms                                                         | 458 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.50 ms: 1.13x slower                                                   |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.14x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 366 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.15x slower                                                   |
| thrift                           | 309 us                                                         | 358 us: 1.16x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 754 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.6 ms: 1.17x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                   |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 118 us: 1.18x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.66 us: 1.19x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 62.3 ms: 1.19x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.6 ms: 1.19x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 114 ms: 1.20x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 51.8 ms: 1.20x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.6 ms: 1.20x slower                                                   |
| 2to3                             | 112 ms                                                         | 134 ms: 1.20x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.95 us: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.22x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 194 ms: 1.22x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.51 ms: 1.23x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.3 ms: 1.24x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.6 ms: 1.24x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 51.1 ns: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 164 us: 1.26x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.50 ms: 1.26x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.6 ms: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.27x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.82 us: 1.30x slower                                                   |
| chaos                            | 24.3 ms                                                        | 31.7 ms: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.1 ms: 1.32x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 68.1 ms: 1.42x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.8 ms: 1.42x slower                                                   |
| raytrace                         | 109 ms                                                         | 157 ms: 1.44x slower                                                    |
| nbody                            | 42.5 ms                                                        | 63.1 ms: 1.48x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.17 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 158 ms: 1.55x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.5 ms: 1.56x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 68.6 ms: 1.60x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 118 ms: 4.09x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, json, dulwich_log, async_tree_memoization_tg, json_loads
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260827-3.16.0a0-24e5a55-NOGIL/bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.055x slower

# HPT report

- Reliability score: 99.39% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.27x