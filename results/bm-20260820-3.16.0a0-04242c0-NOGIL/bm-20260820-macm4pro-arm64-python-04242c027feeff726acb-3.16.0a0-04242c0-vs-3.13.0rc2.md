# Results vs. 3.13.0rc2

- fork: python
- ref: 04242c027feeff726acb
- machine: darwin-arm64
- commit hash: 04242c0
- commit date: 2026-08-20
- overall geometric mean: 1.064x slower
- HPT reliability: 99.78%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.11 sec: 1.06x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 468 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 310 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 315 ms: 1.67x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 315 ms: 1.29x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 321 ms: 1.20x faster                                                    |
| async_generators                 | 193 ms                                                         | 167 ms: 1.15x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 129 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 240 ms: 1.07x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 53.0 ms: 1.23x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 14.0 ms: 1.30x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.6 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                          | 1.19x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.10 ms: 1.18x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.38 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.2 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 119 us: 1.20x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.5 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 166 us: 1.27x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 6.03 ms: 1.37x slower                                                   |
| django_template | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.40x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 781 us: 2.61x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 489 us: 2.03x faster                                                    |
| pylint                           | 106 ms                                                         | 54.8 ms: 1.93x faster                                                   |
| mdp                              | 1.06 sec                                                       | 624 ms: 1.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 310 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 315 ms: 1.67x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.61 ms: 1.36x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 315 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 321 ms: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.10 ms: 1.18x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.38 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 813 ns: 1.17x faster                                                    |
| async_generators                 | 193 ms                                                         | 167 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| go                               | 72.6 ms                                                        | 67.1 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 60.5 us: 1.07x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.6 us: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| pyflate                          | 222 ms                                                         | 213 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 61.9 ms: 1.03x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 20.0 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.11 sec: 1.06x slower                                                  |
| async_tree_eager_memoization     | 122 ms                                                         | 129 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 240 ms: 1.07x slower                                                    |
| fannkuch                         | 179 ms                                                         | 191 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 511 ms: 1.09x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.12x slower                                                    |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| shortest_path                    | 225 ms                                                         | 256 ms: 1.14x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.58 ms: 1.14x slower                                                   |
| sphinx                           | 409 ms                                                         | 468 ms: 1.15x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 370 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.1 ms: 1.15x slower                                                   |
| thrift                           | 309 us                                                         | 357 us: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 761 ms: 1.17x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.87 us: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.63 us: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.9 ms: 1.18x slower                                                   |
| connected_components             | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 119 us: 1.20x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.4 ms: 1.20x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.20x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.1 ms: 1.21x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 36.3 ms: 1.21x slower                                                   |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 53.0 ms: 1.23x slower                                                   |
| 2to3                             | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 196 ms: 1.23x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 50.0 ns: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.23x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.7 ms: 1.24x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.5 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.60 ms: 1.27x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 166 us: 1.27x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.85 us: 1.30x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 14.0 ms: 1.30x slower                                                   |
| chaos                            | 24.3 ms                                                        | 32.2 ms: 1.32x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.5 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 274 us: 1.36x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.03 ms: 1.37x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 571 us: 1.39x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.08 ms: 1.43x slower                                                   |
| django_template                  | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 69.2 ms: 1.44x slower                                                   |
| raytrace                         | 109 ms                                                         | 157 ms: 1.44x slower                                                    |
| nbody                            | 42.5 ms                                                        | 62.6 ms: 1.47x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.9 ms: 1.59x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 70.9 ms: 1.66x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (4): json, json_loads, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.064x slower

# HPT report

- Reliability score: 99.78% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.27x