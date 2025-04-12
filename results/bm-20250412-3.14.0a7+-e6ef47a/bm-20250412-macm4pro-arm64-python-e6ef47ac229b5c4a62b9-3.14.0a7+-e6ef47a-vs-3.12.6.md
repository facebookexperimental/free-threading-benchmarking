# Results vs. 3.12.6

- fork: python
- ref: e6ef47ac229b5c4a62b9
- machine: darwin-arm64
- commit hash: e6ef47a
- commit date: 2025-04-12
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 108 ms: 1.05x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 246 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.6 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.7 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.4 ms: 1.19x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                    |
| tomli_loads          | 957 ms                                                   | 895 ms: 1.07x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.6 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.97 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.73 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.93 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.58 ms: 2.42x faster                                                    |
| mdp                              | 1.09 sec                                                 | 514 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 246 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.47x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.36 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.26x faster                                                    |
| go                               | 70.0 ms                                                  | 56.2 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 940 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.4 ms: 1.19x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.2 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.6 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 895 ms: 1.07x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.94 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| sympy_str                        | 104 ms                                                   | 98.5 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.93 ms: 1.06x faster                                                    |
| 2to3                             | 114 ms                                                   | 108 ms: 1.05x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.7 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.6 us: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.9 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 655 ms: 1.01x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 98.7 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 40.3 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.31 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 879 us: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.97 ms: 1.12x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 228 us: 1.17x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.73 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.6 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250412-3.14.0a7+-e6ef47a/bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x