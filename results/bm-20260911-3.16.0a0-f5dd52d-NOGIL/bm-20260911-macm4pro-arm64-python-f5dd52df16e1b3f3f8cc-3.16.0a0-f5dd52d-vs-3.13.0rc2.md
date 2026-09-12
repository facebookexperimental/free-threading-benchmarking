# Results vs. 3.13.0rc2

- fork: python
- ref: f5dd52df16e1b3f3f8cc
- machine: darwin-arm64
- commit hash: f5dd52d
- commit date: 2026-09-11
- overall geometric mean: 1.072x slower
- HPT reliability: 99.80%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 138 ms: 1.24x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 463 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 309 ms: 1.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 318 ms: 1.65x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 312 ms: 1.30x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 323 ms: 1.20x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.15x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 313 ms: 1.06x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 203 ms: 1.10x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 164 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 264 ms: 1.17x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.8 ms: 1.19x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 151 ms: 1.24x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 283 ms: 1.36x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 167 ms: 1.63x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 71.5 ms: 1.66x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 120 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x slower                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.4 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.36 ms: 1.19x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.9 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.25x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.0 ms: 1.10x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 968 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 40.1 ms: 1.12x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 117 us: 1.18x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.6 ms: 1.25x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 164 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.91 ms: 1.34x slower                                                   |
| django_template | 12.5 ms                                                        | 18.1 ms: 1.45x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.39x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 774 us: 2.64x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 485 us: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 54.7 ms: 1.93x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 309 ms: 1.69x faster                                                    |
| mdp                              | 1.06 sec                                                       | 633 ms: 1.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 318 ms: 1.65x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.67 ms: 1.34x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 312 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.25x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 323 ms: 1.20x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.36 ms: 1.19x faster                                                   |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 812 ns: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.15x faster                                                   |
| async_generators                 | 193 ms                                                         | 169 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.0 ms: 1.10x faster                                                   |
| go                               | 72.6 ms                                                        | 67.1 ms: 1.08x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.9 us: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| pyflate                          | 222 ms                                                         | 211 ms: 1.05x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 15.7 us: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 968 ms: 1.03x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 62.0 ms: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 313 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 501 ms: 1.07x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 203 ms: 1.10x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.12x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 40.1 ms: 1.12x slower                                                   |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 463 ms: 1.13x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.56 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                   |
| shortest_path                    | 225 ms                                                         | 256 ms: 1.14x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 164 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 264 ms: 1.17x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 378 ms: 1.18x slower                                                    |
| thrift                           | 309 us                                                         | 364 us: 1.18x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 117 us: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.19x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.8 ms: 1.19x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.66 us: 1.19x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.4 ms: 1.19x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.93 us: 1.20x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 780 ms: 1.20x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 36.0 ms: 1.21x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 53.0 ms: 1.21x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 63.7 ms: 1.22x slower                                                   |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 117 ms: 1.22x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 30.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 151 ms: 1.24x slower                                                    |
| 2to3                             | 112 ms                                                         | 138 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 198 ms: 1.24x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 31.6 ms: 1.25x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.59 ms: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 164 us: 1.26x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.8 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.1 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.30x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.90 us: 1.31x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 53.3 ns: 1.31x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.91 ms: 1.34x slower                                                   |
| raytrace                         | 109 ms                                                         | 148 ms: 1.36x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 283 ms: 1.36x slower                                                    |
| many_optionals                   | 200 us                                                         | 275 us: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.37x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.04 ms: 1.41x slower                                                   |
| django_template                  | 12.5 ms                                                        | 18.1 ms: 1.45x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 69.9 ms: 1.46x slower                                                   |
| nbody                            | 42.5 ms                                                        | 62.4 ms: 1.47x slower                                                   |
| generators                       | 15.7 ms                                                        | 24.9 ms: 1.59x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 69.7 ms: 1.63x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 167 ms: 1.63x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 71.5 ms: 1.66x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 120 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (4): dulwich_log, deepcopy_reduce, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x slower

# HPT report

- Reliability score: 99.80% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.31x