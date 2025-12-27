# Results vs. 3.12.6

- fork: python
- ref: a1c630834649d54ffbca
- machine: darwin-arm64
- commit hash: a1c6308
- commit date: 2025-12-26
- overall geometric mean: 1.095x faster
- HPT reliability: 99.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.8 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.86 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.16 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.08x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 795 us: 2.53x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 599 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 508 us: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.17 us: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.6 ns: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| go                               | 70.0 ms                                                  | 60.1 ms: 1.16x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 838 ns: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.0 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.11x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.9 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.9 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.72 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.03 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.4 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 683 ms: 1.03x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.8 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.4 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.86 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.16 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 268 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (3): typing_runtime_protocols, xml_etree_process, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251226-3.15.0a3+-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 99.14% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x