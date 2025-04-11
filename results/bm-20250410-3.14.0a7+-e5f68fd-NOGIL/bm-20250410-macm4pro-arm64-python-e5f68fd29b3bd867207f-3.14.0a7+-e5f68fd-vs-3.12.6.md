# Results vs. 3.12.6

- fork: python
- ref: e5f68fd29b3bd867207f
- machine: darwin-arm64
- commit hash: e5f68fd
- commit date: 2025-04-10
- overall geometric mean: 1.118x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.47x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 84.7 ms: 2.03x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.2 ms: 1.80x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 228 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 237 ms: 1.41x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 221 ms: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.40x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 53.0 ms: 1.02x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|---------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse | 51.6 ms                                                  | 36.2 ms: 1.42x faster                                                    |
| xml_etree_parse     | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                    |
| xml_etree_generate  | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| xml_etree_process   | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                    |
| tomli_loads         | 957 ms                                                   | 950 ms: 1.01x faster                                                     |
| pickle_pure_python  | 139 us                                                   | 148 us: 1.07x slower                                                     |
| json_loads          | 10.9 us                                                  | 11.9 us: 1.09x slower                                                    |
| json_dumps          | 4.26 ms                                                  | 5.04 ms: 1.18x slower                                                    |
| Geometric mean      | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.46 ms: 1.18x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.52 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| mako            | 4.77 ms                                                  | 5.39 ms: 1.13x slower                                                    |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 747 us: 2.69x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.47x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.59 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 84.7 ms: 2.03x faster                                                    |
| mdp                              | 1.09 sec                                                 | 559 ms: 1.95x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 442 us: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.2 ms: 1.80x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 228 ms: 1.48x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.2 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 237 ms: 1.41x faster                                                     |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.5 us: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.20 us: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 805 ns: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                   |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                     |
| go                               | 70.0 ms                                                  | 60.7 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| k_core                           | 1.12 sec                                                 | 977 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.7 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.9 ms: 1.11x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 46.1 ns: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.59 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| docutils                         | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.9 ms: 1.04x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| nbody                            | 54.2 ms                                                  | 53.0 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.91 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 950 ms: 1.01x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.79 us: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.05 ms: 1.00x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.09 ms: 1.00x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.3 us: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 40.0 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.03x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 53.2 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 221 ms: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.8 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| shortest_path                    | 219 ms                                                   | 229 ms: 1.05x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.2 ms: 1.05x slower                                                    |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.07x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 351 ms: 1.07x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 719 ms: 1.08x slower                                                     |
| connected_components             | 201 ms                                                   | 217 ms: 1.08x slower                                                     |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.65 ms: 1.09x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.39 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.4 ms: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.46 ms: 1.18x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.04 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.25 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.52 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 570 us: 1.36x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250410-3.14.0a7+-e5f68fd-NOGIL/bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.23x