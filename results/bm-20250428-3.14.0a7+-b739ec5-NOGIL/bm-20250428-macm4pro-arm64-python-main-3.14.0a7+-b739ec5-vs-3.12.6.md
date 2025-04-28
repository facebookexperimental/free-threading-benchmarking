# Results vs. 3.12.6

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: b739ec5
- commit date: 2025-04-28
- overall geometric mean: 1.082x faster
- HPT reliability: 87.28%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                   |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                    |
| sphinx         | 434 ms                                                   | 428 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                     |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                     |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.69x faster                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 113 ms: 1.01x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.3 ms: 2.44x slower                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                     |
| nbody          | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                    |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                    |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                     |
| regex_v8       | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                    |
| tomli_loads          | 957 ms                                                   | 1000 ms: 1.04x slower                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                     |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                     |
| json_loads           | 10.9 us                                                  | 12.4 us: 1.14x slower                                    |
| json_dumps           | 4.26 ms                                                  | 5.17 ms: 1.21x slower                                    |
| Geometric mean       | (ref)                                                    | 1.00x slower                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.17x slower                                    |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                    |
| Geometric mean  | (ref)                                                    | 1.14x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.61x faster                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                     |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                     |
| subparsers                       | 20.8 ms                                                  | 8.97 ms: 2.32x faster                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                     |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                    |
| mdp                              | 1.09 sec                                                 | 582 ms: 1.88x faster                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                     |
| create_gc_cycles                 | 830 us                                                   | 453 us: 1.83x faster                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.69x faster                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                     |
| float                            | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                    |
| deepcopy                         | 161 us                                                   | 126 us: 1.29x faster                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.6 us: 1.25x faster                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                     |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                     |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                    |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                    |
| comprehensions                   | 9.84 us                                                  | 8.78 us: 1.12x faster                                    |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                     |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                     |
| raytrace                         | 145 ms                                                   | 130 ms: 1.12x faster                                     |
| go                               | 70.0 ms                                                  | 63.3 ms: 1.11x faster                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.2 ms: 1.11x faster                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.3 ms: 1.10x faster                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                    |
| pycparser                        | 497 ms                                                   | 475 ms: 1.05x faster                                     |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                    |
| pyflate                          | 216 ms                                                   | 209 ms: 1.04x faster                                     |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                     |
| sphinx                           | 434 ms                                                   | 428 ms: 1.01x faster                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 113 ms: 1.01x slower                                     |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.20 ms: 1.02x slower                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                     |
| regex_v8                         | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                    |
| scimark_fft                      | 142 ms                                                   | 147 ms: 1.03x slower                                     |
| logging_simple                   | 2.57 us                                                  | 2.66 us: 1.04x slower                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                    |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                    |
| tomli_loads                      | 957 ms                                                   | 1000 ms: 1.04x slower                                    |
| logging_format                   | 2.80 us                                                  | 2.93 us: 1.05x slower                                    |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.05x slower                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.3 us: 1.05x slower                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                    |
| nbody                            | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                    |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                     |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.07x slower                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.7 ms: 1.07x slower                                    |
| hexiom                           | 3.04 ms                                                  | 3.24 ms: 1.07x slower                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                     |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                     |
| sympy_sum                        | 57.6 ms                                                  | 62.3 ms: 1.08x slower                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                    |
| fannkuch                         | 176 ms                                                   | 192 ms: 1.09x slower                                     |
| richards                         | 22.4 ms                                                  | 24.5 ms: 1.09x slower                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                    |
| richards_super                   | 25.4 ms                                                  | 27.8 ms: 1.10x slower                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.4 ms: 1.10x slower                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                    |
| pprint_safe_repr                 | 328 ms                                                   | 363 ms: 1.11x slower                                     |
| pprint_pformat                   | 665 ms                                                   | 743 ms: 1.12x slower                                     |
| json_loads                       | 10.9 us                                                  | 12.4 us: 1.14x slower                                    |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.15x slower                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.97 ms: 1.15x slower                                    |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.17x slower                                    |
| python_startup                   | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                    |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                    |
| json_dumps                       | 4.26 ms                                                  | 5.17 ms: 1.21x slower                                    |
| meteor_contest                   | 47.7 ms                                                  | 58.0 ms: 1.21x slower                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                    |
| telco                            | 2.61 ms                                                  | 3.29 ms: 1.26x slower                                    |
| many_optionals                   | 195 us                                                   | 249 us: 1.27x slower                                     |
| bench_thread_pool                | 419 us                                                   | 598 us: 1.43x slower                                     |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.48x slower                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.3 ms: 2.44x slower                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250428-3.14.0a7+-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7+-b739ec5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 87.28% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x