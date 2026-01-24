# Results vs. 3.12.6

- fork: python
- ref: 012c498035a9adfe9fd2
- machine: darwin-arm64
- commit hash: 012c498
- commit date: 2026-01-24
- overall geometric mean: 1.254x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 992 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 19.2 ms: 1.20x faster                                                    |
| sphinx         | 434 ms                                                   | 384 ms: 1.13x faster                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 217 ms: 2.21x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 96.4 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.0 ms: 1.79x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.3 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 22.9 ms: 1.65x faster                                                    |
| nbody          | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.8 ms: 1.34x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.50 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 666 ms: 1.44x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 74.0 us: 1.39x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 31.3 ms: 1.24x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 113 us: 1.23x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.63 ms: 1.17x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 8.81 ms: 1.19x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| django_template | 13.6 ms                                                  | 13.8 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.92 ms: 5.30x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.33 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.28x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.2 ms: 2.28x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 217 ms: 2.21x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 27.7 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 96.4 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.0 ms: 1.79x faster                                                    |
| mdp                              | 1.09 sec                                                 | 615 ms: 1.77x faster                                                     |
| deepcopy                         | 161 us                                                   | 92.8 us: 1.74x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.6 us: 1.72x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| float                            | 37.9 ms                                                  | 22.9 ms: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.64x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 38.2 ms: 1.59x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.32 us: 1.56x faster                                                    |
| go                               | 70.0 ms                                                  | 45.7 ms: 1.53x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.14 ms: 1.52x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 983 ns: 1.49x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 97.5 ms: 1.45x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 35.3 ns: 1.44x faster                                                    |
| pyflate                          | 216 ms                                                   | 150 ms: 1.44x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 666 ms: 1.44x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.9 ms: 1.41x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 74.0 us: 1.39x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 39.4 ms: 1.38x faster                                                    |
| raytrace                         | 145 ms                                                   | 106 ms: 1.36x faster                                                     |
| nbody                            | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 40.8 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| chaos                            | 28.9 ms                                                  | 21.9 ms: 1.32x faster                                                    |
| k_core                           | 1.12 sec                                                 | 859 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 262 ms: 1.25x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 532 ms: 1.25x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 31.3 ms: 1.24x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 31.4 ms: 1.24x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 113 us: 1.23x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.09 us: 1.23x faster                                                    |
| mako                             | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 37.3 ms: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.6 ms: 1.22x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.84 sec: 1.22x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.30 us: 1.22x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 19.2 ms: 1.20x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 8.81 ms: 1.19x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.63 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| pycparser                        | 497 ms                                                   | 433 ms: 1.15x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| sphinx                           | 434 ms                                                   | 384 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| fannkuch                         | 176 ms                                                   | 156 ms: 1.12x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.12x faster                                                    |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.58 ms: 1.06x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 45.7 ms: 1.05x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 992 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.9 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.50 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.01x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.64 ms: 1.01x slower                                                    |
| django_template                  | 13.6 ms                                                  | 13.8 ms: 1.01x slower                                                    |
| sympy_str                        | 104 ms                                                   | 106 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 910 us: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260124-3.15.0a5+-012c498-JIT/bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.254x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.26x