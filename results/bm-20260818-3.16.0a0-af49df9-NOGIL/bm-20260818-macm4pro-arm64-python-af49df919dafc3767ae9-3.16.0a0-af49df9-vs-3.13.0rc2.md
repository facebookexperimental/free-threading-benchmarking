# Results vs. 3.13.0rc2

- fork: python
- ref: af49df919dafc3767ae9
- machine: darwin-arm64
- commit hash: af49df9
- commit date: 2026-08-18
- overall geometric mean: 1.061x slower
- HPT reliability: 99.71%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 136 ms: 1.22x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.06x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 464 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 306 ms: 1.70x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 312 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 312 ms: 1.30x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 317 ms: 1.22x faster                                                    |
| async_generators                 | 193 ms                                                         | 163 ms: 1.18x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 191 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 148 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 239 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 146 ms: 1.10x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.9 ms: 1.20x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 52.0 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 64.2 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                          | 1.20x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 68.6 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 922 ms: 1.08x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.2 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 117 us: 1.18x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.6 ms: 1.25x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 165 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.90 ms: 1.34x slower                                                   |
| django_template | 12.5 ms                                                        | 17.9 ms: 1.43x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.38x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 784 us: 2.60x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 493 us: 2.02x faster                                                    |
| pylint                           | 106 ms                                                         | 54.5 ms: 1.94x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 306 ms: 1.70x faster                                                    |
| mdp                              | 1.06 sec                                                       | 627 ms: 1.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 312 ms: 1.68x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.44x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.62 ms: 1.35x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 312 ms: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 317 ms: 1.22x faster                                                    |
| async_generators                 | 193 ms                                                         | 163 ms: 1.18x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 809 ns: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.9 us: 1.10x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                   |
| go                               | 72.6 ms                                                        | 66.8 ms: 1.09x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 922 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 60.9 us: 1.06x faster                                                   |
| pyflate                          | 222 ms                                                         | 212 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 62.1 ms: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| dulwich_log                      | 19.8 ms                                                        | 20.1 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.14 ms: 1.02x slower                                                   |
| async_tree_memoization           | 184 ms                                                         | 191 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 148 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.06x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 239 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 193 ms: 1.08x slower                                                    |
| pycparser                        | 470 ms                                                         | 509 ms: 1.08x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.2 ms: 1.10x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 146 ms: 1.10x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.12x slower                                                    |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 364 ms: 1.13x slower                                                    |
| sphinx                           | 409 ms                                                         | 464 ms: 1.14x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.55 ms: 1.14x slower                                                   |
| shortest_path                    | 225 ms                                                         | 256 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 750 ms: 1.15x slower                                                    |
| thrift                           | 309 us                                                         | 359 us: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.89 us: 1.18x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 117 us: 1.18x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                   |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.5 ms: 1.19x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.9 ms: 1.20x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 62.8 ms: 1.20x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 52.0 ms: 1.20x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 116 ms: 1.21x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.8 ms: 1.21x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 194 ms: 1.22x slower                                                    |
| 2to3                             | 112 ms                                                         | 136 ms: 1.22x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 49.6 ns: 1.22x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.4 ms: 1.23x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 53.9 ms: 1.23x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.6 ms: 1.25x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.56 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 165 us: 1.26x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.78 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.3 ms: 1.32x slower                                                   |
| chaos                            | 24.3 ms                                                        | 32.2 ms: 1.33x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.90 ms: 1.34x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 271 us: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 578 us: 1.40x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 68.6 ms: 1.43x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.9 ms: 1.43x slower                                                   |
| raytrace                         | 109 ms                                                         | 160 ms: 1.47x slower                                                    |
| nbody                            | 42.5 ms                                                        | 64.2 ms: 1.51x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.21 ms: 1.53x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.8 ms: 1.58x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 74.7 ms: 1.75x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, json, json_loads
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.061x slower

# HPT report

- Reliability score: 99.71% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.27x