# Results vs. 3.12.6

- fork: python
- ref: a1c630834649d54ffbca
- machine: darwin-arm64
- commit hash: a1c6308
- commit date: 2025-12-26
- overall geometric mean: 1.167x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 389 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.2 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.2 ms: 1.21x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.1 us: 1.06x faster                                                    |
| tomli_loads          | 957 ms                                                   | 920 ms: 1.04x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.63 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.04 ms: 5.14x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| mdp                              | 1.09 sec                                                 | 538 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.58x faster                                                    |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.05 us: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| go                               | 70.0 ms                                                  | 52.6 ms: 1.33x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.6 ms: 1.26x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 899 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 45.2 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.4 ms: 1.18x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.4 us: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 389 ms: 1.11x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.76 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.63 ms: 1.09x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 612 ms: 1.09x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 304 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.1 us: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.0 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 920 ms: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 930 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.2 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): sqlite_synth, pidigits
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251226-3.15.0a3+-a1c6308/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.167x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.21x