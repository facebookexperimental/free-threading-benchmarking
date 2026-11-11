# Results vs. 3.13.0rc2

- fork: python
- ref: acab53212d89b298ba0d
- machine: darwin-arm64
- commit hash: acab532
- commit date: 2026-11-10
- overall geometric mean: 1.016x slower
- HPT reliability: 94.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 127 ms: 1.14x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| sphinx         | 409 ms                                                         | 452 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                          | 1.06x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 300 ms: 1.74x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 303 ms: 1.73x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.72x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 303 ms: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 303 ms: 1.27x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 300 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 143 ms: 1.08x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.0 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 272 ms: 1.31x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 115 ms: 3.98x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 150 ms: 1.11x faster                                                        |
| float          | 31.4 ms                                                        | 33.7 ms: 1.07x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.7 ms: 1.38x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.6 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 64.2 ms: 1.34x slower                                                       |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 877 ms: 1.14x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.1 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.5 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 159 us: 1.22x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                       |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 805 us: 2.54x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 475 us: 2.09x faster                                                        |
| pylint                           | 106 ms                                                         | 53.4 ms: 1.98x faster                                                       |
| mdp                              | 1.06 sec                                                       | 582 ms: 1.82x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 300 ms: 1.74x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 303 ms: 1.73x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.72x faster                                                        |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                      |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 303 ms: 1.34x faster                                                        |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 303 ms: 1.27x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.8 us: 1.20x faster                                                       |
| go                               | 72.6 ms                                                        | 60.4 ms: 1.20x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 877 ms: 1.14x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.13x faster                                                      |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                       |
| pidigits                         | 166 ms                                                         | 150 ms: 1.11x faster                                                        |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.9 us: 1.11x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.6 ms: 1.09x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 91.6 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.03x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                       |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 300 ms: 1.02x slower                                                        |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                       |
| pycparser                        | 470 ms                                                         | 495 ms: 1.05x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.1 ms: 1.06x slower                                                       |
| float                            | 31.4 ms                                                        | 33.7 ms: 1.07x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.08x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 143 ms: 1.08x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.16 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.09x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.8 ms: 1.11x slower                                                       |
| sphinx                           | 409 ms                                                         | 452 ms: 1.11x slower                                                        |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.8 ms: 1.13x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.3 ms: 1.13x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                       |
| 2to3                             | 112 ms                                                         | 127 ms: 1.14x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.1 ms: 1.14x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 470 us: 1.14x slower                                                        |
| connected_components             | 208 ms                                                         | 239 ms: 1.15x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 50.0 ms: 1.16x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.5 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 61.4 ms: 1.17x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.5 ms: 1.18x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 43.8 ms: 1.18x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 159 us: 1.22x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 41.0 ms: 1.22x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.30 us: 1.22x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 50.1 ns: 1.23x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.80 ms: 1.24x slower                                                       |
| mako                             | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                       |
| raytrace                         | 109 ms                                                         | 137 ms: 1.25x slower                                                        |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 272 ms: 1.31x slower                                                        |
| coverage                         | 31.2 ms                                                        | 41.6 ms: 1.33x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 64.2 ms: 1.34x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.7 ms: 1.38x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.9 ms: 1.52x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 68.1 ms: 1.59x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 115 ms: 3.98x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (5): async_tree_memoization_tg, html5lib, dulwich_log, async_tree_memoization, async_tree_none
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261110-3.16.0a2+dev-acab532-NOGIL/bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 94.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x