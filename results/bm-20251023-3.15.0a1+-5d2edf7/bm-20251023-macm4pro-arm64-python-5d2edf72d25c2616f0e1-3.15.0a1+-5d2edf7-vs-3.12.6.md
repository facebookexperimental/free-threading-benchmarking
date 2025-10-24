# Results vs. 3.12.6

- fork: python
- ref: 5d2edf72d25c2616f0e1
- machine: darwin-arm64
- commit hash: 5d2edf7
- commit date: 2025-10-23
- overall geometric mean: 1.097x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 232 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.09x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.63x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.55x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.4 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.6 ms: 2.60x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                    |
| nbody          | 54.2 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 232 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.09x faster                                                     |
| mdp                              | 1.09 sec                                                 | 544 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.63x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.55x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.61 us: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.2 ms: 1.23x faster                                                    |
| k_core                           | 1.12 sec                                                 | 909 ms: 1.23x faster                                                     |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.3 ns: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.9 ms: 1.16x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 52.7 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.4 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.05 sec: 1.09x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.2 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.0 us: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| nbody                            | 54.2 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.4 ms: 1.05x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.91 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.8 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.03x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.0 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.8 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 317 us: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                     |
| sympy_str                        | 104 ms                                                   | 104 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 677 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.1 ms: 1.03x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 176 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.5 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.07x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 913 us: 1.10x slower                                                     |
| fannkuch                         | 176 ms                                                   | 195 ms: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.94 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.7 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 366 us: 1.87x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.6 ms: 2.60x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (5): sympy_sum, json, bench_thread_pool, tomli_loads, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251023-3.15.0a1+-5d2edf7/bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x