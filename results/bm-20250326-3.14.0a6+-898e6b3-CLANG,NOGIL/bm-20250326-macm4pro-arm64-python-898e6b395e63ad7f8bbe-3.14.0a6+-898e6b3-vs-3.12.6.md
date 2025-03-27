# Results vs. 3.12.6

- fork: python
- ref: 898e6b395e63ad7f8bbe
- machine: darwin-arm64
- commit hash: 898e6b3
- commit date: 2025-03-26
- overall geometric mean: 1.132x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 974 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 189 ms: 2.54x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 198 ms: 2.51x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 186 ms: 2.40x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.25x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 82.7 ms: 2.08x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 121 ms: 1.91x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.6 ms: 1.79x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.08 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 109 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.5 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 220 ms: 1.04x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 74.4 ms: 2.32x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.43x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 61.5 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 34.7 ms: 1.49x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 55.7 ms: 1.22x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.4 ms: 1.13x faster                                                    |
| tomli_loads          | 957 ms                                                   | 881 ms: 1.09x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.8 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.04 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.16 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.25 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| mako            | 4.77 ms                                                  | 5.43 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 758 us: 2.65x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 189 ms: 2.54x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 198 ms: 2.51x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.39 ms: 2.47x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 186 ms: 2.40x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.25x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 82.7 ms: 2.08x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 121 ms: 1.91x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 457 us: 1.82x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.6 ms: 1.79x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                    |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.08 ms: 1.49x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 34.7 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.89 us: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 55.7 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                     |
| go                               | 70.0 ms                                                  | 58.1 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 806 ns: 1.20x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 53.4 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.4 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| pycparser                        | 497 ms                                                   | 449 ms: 1.11x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 881 ms: 1.09x faster                                                     |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 974 ms: 1.05x faster                                                     |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.8 us: 1.04x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.92 ms: 1.04x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.9 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 68.6 us: 1.04x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 109 ms: 1.03x faster                                                     |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.87 ms: 1.02x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.6 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.1 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 39.6 ms: 1.00x faster                                                    |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.10 sec: 1.00x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 47.5 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.5 ms: 1.02x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.7 ms: 1.02x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 337 ms: 1.03x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 220 ms: 1.04x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.37 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| shortest_path                    | 219 ms                                                   | 237 ms: 1.08x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.1 ms: 1.11x slower                                                    |
| nbody                            | 54.2 ms                                                  | 61.5 ms: 1.13x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.43 ms: 1.14x slower                                                    |
| connected_components             | 201 ms                                                   | 229 ms: 1.14x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.16 ms: 1.14x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.04 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.28 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.25 ms: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.3 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 74.4 ms: 2.32x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (3): sympy_str, asyncio_websockets, json
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250326-3.14.0a6+-898e6b3-CLANG,NOGIL/bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.22x