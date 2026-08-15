# Results vs. 3.13.0rc2

- fork: python
- ref: dffac6163e693cf80ed4
- machine: darwin-arm64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.067x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.11 sec: 1.06x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 464 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 311 ms: 1.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 316 ms: 1.66x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 315 ms: 1.28x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 321 ms: 1.20x faster                                                    |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 194 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 310 ms: 1.05x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 151 ms: 1.06x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 129 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 241 ms: 1.07x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 148 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 52.9 ms: 1.23x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.7 ms: 1.27x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 282 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 120 ms: 4.16x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| float          | 31.4 ms                                                        | 35.1 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 64.1 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                          | 1.20x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.08 ms: 1.18x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.4 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.1 ms: 1.07x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 118 us: 1.19x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 166 us: 1.27x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.29 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 6.05 ms: 1.37x slower                                                   |
| django_template | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 795 us: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 490 us: 2.03x faster                                                    |
| pylint                           | 106 ms                                                         | 55.1 ms: 1.92x faster                                                   |
| mdp                              | 1.06 sec                                                       | 624 ms: 1.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 311 ms: 1.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 316 ms: 1.66x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.43x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.58 ms: 1.37x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 315 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 321 ms: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.08 ms: 1.18x faster                                                   |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 808 ns: 1.17x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| go                               | 72.6 ms                                                        | 67.3 ms: 1.08x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.3 us: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.1 ms: 1.07x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.5 us: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| pyflate                          | 222 ms                                                         | 215 ms: 1.03x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 62.1 ms: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.12 ms: 1.02x slower                                                   |
| dulwich_log                      | 19.8 ms                                                        | 20.2 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 194 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 310 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.4 ms: 1.06x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.11 sec: 1.06x slower                                                  |
| async_tree_none                  | 142 ms                                                         | 151 ms: 1.06x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 129 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 241 ms: 1.07x slower                                                    |
| fannkuch                         | 179 ms                                                         | 192 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 509 ms: 1.08x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 148 ms: 1.11x slower                                                    |
| float                            | 31.4 ms                                                        | 35.1 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 464 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 256 ms: 1.14x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.66 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.1 ms: 1.15x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 371 ms: 1.15x slower                                                    |
| thrift                           | 309 us                                                         | 357 us: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.7 ms: 1.17x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 764 ms: 1.18x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.64 us: 1.18x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.4 ms: 1.18x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 118 us: 1.19x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.1 ms: 1.19x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.93 us: 1.20x slower                                                   |
| connected_components             | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.29 ms: 1.22x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 117 ms: 1.23x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 52.9 ms: 1.23x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 196 ms: 1.23x slower                                                    |
| 2to3                             | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 64.4 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.6 ms: 1.24x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 50.4 ns: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.60 ms: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 166 us: 1.27x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 13.7 ms: 1.27x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.80 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.31x slower                                                   |
| chaos                            | 24.3 ms                                                        | 32.0 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 282 ms: 1.35x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.05 ms: 1.37x slower                                                   |
| many_optionals                   | 200 us                                                         | 276 us: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                    |
| django_template                  | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| raytrace                         | 109 ms                                                         | 157 ms: 1.44x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 69.4 ms: 1.45x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.16 ms: 1.49x slower                                                   |
| nbody                            | 42.5 ms                                                        | 64.1 ms: 1.51x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.8 ms: 1.58x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 69.3 ms: 1.62x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 120 ms: 4.16x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.067x slower

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.27x