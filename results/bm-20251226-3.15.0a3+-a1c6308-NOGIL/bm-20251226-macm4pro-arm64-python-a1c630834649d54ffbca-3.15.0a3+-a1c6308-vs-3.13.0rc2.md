# Results vs. 3.13.0rc2

- fork: python
- ref: a1c630834649d54ffbca
- machine: darwin-arm64
- commit hash: a1c6308
- commit date: 2025-12-26
- overall geometric mean: 1.016x faster
- HPT reliability: 57.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| sphinx         | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.8 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.86 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.16 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 795 us: 2.57x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 508 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.77x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 60.1 ms: 1.21x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.0 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 838 ns: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| async_generators                 | 193 ms                                                         | 187 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.00x slower                                                     |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 683 ms: 1.05x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.6 ns: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.4 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.8 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.6 us: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.72 us: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.03 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.86 ms: 1.14x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.8 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.9 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.17 us: 1.20x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.16 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.4 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.7 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.5 ms: 1.32x slower                                                    |
| many_optionals                   | 200 us                                                         | 268 us: 1.34x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (3): tomli_loads, regex_dna, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251226-3.15.0a3+-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 57.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x