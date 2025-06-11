# Results vs. 3.12.6

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: darwin-arm64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.100x faster
- HPT reliability: 98.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.1 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.13 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.7 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 981 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.38 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.85 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 776 us: 2.59x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.58 ms: 2.17x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| mdp                              | 1.09 sec                                                 | 564 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 489 us: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.39x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.90 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 61.4 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 984 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 130 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.3 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.13 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.7 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.90 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.01x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.06 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 328 us: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 981 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.0 us: 1.03x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 59.7 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.1 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.78 us: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.09 us: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.11x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.2 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 376 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 764 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.38 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.85 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 62.1 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 249 us: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 596 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.7 ms: 1.52x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 98.90% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x