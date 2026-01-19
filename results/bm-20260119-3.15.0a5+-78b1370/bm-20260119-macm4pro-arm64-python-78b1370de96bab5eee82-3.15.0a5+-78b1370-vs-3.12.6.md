# Results vs. 3.12.6

- fork: python
- ref: 78b1370de96bab5eee82
- machine: darwin-arm64
- commit hash: 78b1370
- commit date: 2026-01-19
- overall geometric mean: 1.186x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| docutils       | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 382 ms: 1.14x faster                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.9 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.8 ms: 1.41x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.3 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.3 ms: 1.23x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.0 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 94.1 us: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.50 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.26x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| mdp                              | 1.09 sec                                                 | 527 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.9 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.1 us: 1.68x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.92 us: 1.42x faster                                                    |
| float                            | 37.9 ms                                                  | 26.8 ms: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.40x faster                                                    |
| go                               | 70.0 ms                                                  | 51.0 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| raytrace                         | 145 ms                                                   | 112 ms: 1.30x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 39.4 ns: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.3 ms: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.1 ms: 1.24x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.3 ms: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.3 ms: 1.22x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.1 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| pyflate                          | 216 ms                                                   | 180 ms: 1.20x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.1 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.19x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 61.0 us: 1.16x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.3 ms: 1.16x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.5 ms: 1.16x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.0 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.5 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.15x faster                                                    |
| sphinx                           | 434 ms                                                   | 382 ms: 1.14x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 449 ms: 1.11x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.24 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.50 ms: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 94.1 us: 1.09x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 35.7 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.0 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 617 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.7 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.1 ms: 1.06x faster                                                    |
| fannkuch                         | 176 ms                                                   | 166 ms: 1.06x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.00 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.0 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 899 us: 1.08x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.1 ms: 1.16x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260119-3.15.0a5+-78b1370/bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.186x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.23x