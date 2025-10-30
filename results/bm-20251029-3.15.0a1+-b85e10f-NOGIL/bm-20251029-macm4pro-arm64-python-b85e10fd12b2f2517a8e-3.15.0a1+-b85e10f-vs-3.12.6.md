# Results vs. 3.12.6

- fork: python
- ref: b85e10fd12b2f2517a8e
- machine: darwin-arm64
- commit hash: b85e10f
- commit date: 2025-10-29
- overall geometric mean: 1.078x faster
- HPT reliability: 95.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 415 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.41x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.98x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.07x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.09x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 61.3 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.39 ms: 1.02x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 53.8 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| tomli_loads          | 957 ms                                                   | 973 ms: 1.02x slower                                                     |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.7 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.85 ms: 1.22x slower                                                    |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 757 us: 2.65x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.41x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.98x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 612 ms: 1.79x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 469 us: 1.77x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.44x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| deepcopy                         | 161 us                                                   | 119 us: 1.35x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.50 us: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 848 ns: 1.14x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                     |
| go                               | 70.0 ms                                                  | 62.3 ms: 1.12x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.5 ns: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.02 sec: 1.11x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.9 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                     |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 134 ms: 1.06x faster                                                     |
| sphinx                           | 434 ms                                                   | 415 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.39 ms: 1.02x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.53 us: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 53.8 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 530 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 973 ms: 1.02x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.4 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.5 us: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.20 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 344 us: 1.07x slower                                                     |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                     |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.24 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.09x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 359 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.6 ms: 1.10x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 731 ms: 1.10x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 56.4 ms: 1.10x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                     |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                    |
| nbody                            | 54.2 ms                                                  | 61.3 ms: 1.13x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.7 ms: 1.13x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.1 ms: 1.20x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.85 ms: 1.22x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 548 us: 1.31x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.9 ms: 1.52x slower                                                    |
| many_optionals                   | 195 us                                                   | 381 us: 1.95x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251029-3.15.0a1+-b85e10f-NOGIL/bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 95.07% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x