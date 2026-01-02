# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: call_function_ex_py
- machine: darwin-arm64
- commit hash: 884a7a7
- commit date: 2026-01-02
- overall geometric mean: 1.273x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 107 ms: 1.07x faster                                                              |
| docutils       | 1.02 sec                                                 | 973 ms: 1.05x faster                                                              |
| html5lib       | 23.0 ms                                                  | 19.4 ms: 1.18x faster                                                             |
| sphinx         | 434 ms                                                   | 379 ms: 1.14x faster                                                              |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 212 ms: 2.34x faster                                                              |
| async_tree_io_tg                 | 480 ms                                                   | 215 ms: 2.23x faster                                                              |
| async_tree_eager_io_tg           | 446 ms                                                   | 213 ms: 2.10x faster                                                              |
| async_tree_io                    | 459 ms                                                   | 222 ms: 2.07x faster                                                              |
| async_tree_none                  | 178 ms                                                   | 94.5 ms: 1.89x faster                                                             |
| async_tree_none_tg               | 172 ms                                                   | 94.7 ms: 1.82x faster                                                             |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                              |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                              |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.39x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                              |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                             |
| async_tree_eager                 | 45.6 ms                                                  | 35.9 ms: 1.27x faster                                                             |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                              |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 214 ms: 1.08x faster                                                              |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                              |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                              |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.2 ms: 2.37x slower                                                             |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 22.8 ms: 1.66x faster                                                             |
| nbody          | 54.2 ms                                                  | 39.0 ms: 1.39x faster                                                             |
| pidigits       | 161 ms                                                   | 155 ms: 1.04x faster                                                              |
| Geometric mean | (ref)                                                    | 1.34x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.1 ms: 1.40x faster                                                             |
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                             |
| regex_dna      | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                             |
| regex_v8       | 9.59 ms                                                  | 9.51 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                    | 1.16x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 70.5 us: 1.46x faster                                                             |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                             |
| xml_etree_generate   | 38.9 ms                                                  | 30.2 ms: 1.29x faster                                                             |
| pickle_pure_python   | 139 us                                                   | 110 us: 1.26x faster                                                              |
| xml_etree_process    | 26.7 ms                                                  | 21.4 ms: 1.25x faster                                                             |
| tomli_loads          | 957 ms                                                   | 785 ms: 1.22x faster                                                              |
| json_dumps           | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                             |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                             |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.04x faster                                                             |
| Geometric mean       | (ref)                                                    | 1.24x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                             |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                             |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.86 ms: 1.24x faster                                                             |
| genshi_text     | 10.5 ms                                                  | 8.90 ms: 1.18x faster                                                             |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                             |
| django_template | 13.6 ms                                                  | 13.5 ms: 1.01x faster                                                             |
| Geometric mean  | (ref)                                                    | 1.11x faster                                                                      |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.79 ms: 5.49x faster                                                             |
| async_tree_eager_io              | 496 ms                                                   | 212 ms: 2.34x faster                                                              |
| richards                         | 22.4 ms                                                  | 9.66 ms: 2.32x faster                                                             |
| async_tree_io_tg                 | 480 ms                                                   | 215 ms: 2.23x faster                                                              |
| richards_super                   | 25.4 ms                                                  | 11.4 ms: 2.23x faster                                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 213 ms: 2.10x faster                                                              |
| async_tree_io                    | 459 ms                                                   | 222 ms: 2.07x faster                                                              |
| mdp                              | 1.09 sec                                                 | 567 ms: 1.93x faster                                                              |
| async_tree_none                  | 178 ms                                                   | 94.5 ms: 1.89x faster                                                             |
| async_tree_none_tg               | 172 ms                                                   | 94.7 ms: 1.82x faster                                                             |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                              |
| deepcopy                         | 161 us                                                   | 95.3 us: 1.69x faster                                                             |
| go                               | 70.0 ms                                                  | 41.4 ms: 1.69x faster                                                             |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                              |
| float                            | 37.9 ms                                                  | 22.8 ms: 1.66x faster                                                             |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                             |
| comprehensions                   | 9.84 us                                                  | 6.06 us: 1.62x faster                                                             |
| deltablue                        | 1.73 ms                                                  | 1.10 ms: 1.57x faster                                                             |
| pyflate                          | 216 ms                                                   | 142 ms: 1.52x faster                                                              |
| logging_silent                   | 50.9 ns                                                  | 34.3 ns: 1.48x faster                                                             |
| deepcopy_reduce                  | 1.46 us                                                  | 991 ns: 1.47x faster                                                              |
| scimark_sor                      | 61.0 ms                                                  | 41.7 ms: 1.46x faster                                                             |
| unpickle_pure_python             | 103 us                                                   | 70.5 us: 1.46x faster                                                             |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.1 ms: 1.46x faster                                                             |
| scimark_fft                      | 142 ms                                                   | 99.4 ms: 1.43x faster                                                             |
| scimark_lu                       | 51.3 ms                                                  | 36.0 ms: 1.43x faster                                                             |
| regex_compile                    | 54.6 ms                                                  | 39.1 ms: 1.40x faster                                                             |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.39x faster                                                              |
| nbody                            | 54.2 ms                                                  | 39.0 ms: 1.39x faster                                                             |
| raytrace                         | 145 ms                                                   | 104 ms: 1.39x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                              |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                             |
| chaos                            | 28.9 ms                                                  | 21.5 ms: 1.35x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                             |
| spectral_norm                    | 54.4 ms                                                  | 41.3 ms: 1.32x faster                                                             |
| k_core                           | 1.12 sec                                                 | 861 ms: 1.30x faster                                                              |
| xml_etree_generate               | 38.9 ms                                                  | 30.2 ms: 1.29x faster                                                             |
| crypto_pyaes                     | 38.8 ms                                                  | 30.2 ms: 1.28x faster                                                             |
| pprint_safe_repr                 | 328 ms                                                   | 256 ms: 1.28x faster                                                              |
| async_tree_eager                 | 45.6 ms                                                  | 35.9 ms: 1.27x faster                                                             |
| pprint_pformat                   | 665 ms                                                   | 525 ms: 1.27x faster                                                              |
| pickle_pure_python               | 139 us                                                   | 110 us: 1.26x faster                                                              |
| logging_simple                   | 2.57 us                                                  | 2.04 us: 1.26x faster                                                             |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                              |
| xml_etree_process                | 26.7 ms                                                  | 21.4 ms: 1.25x faster                                                             |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.80 sec: 1.24x faster                                                            |
| logging_format                   | 2.80 us                                                  | 2.26 us: 1.24x faster                                                             |
| mako                             | 4.77 ms                                                  | 3.86 ms: 1.24x faster                                                             |
| tomli_loads                      | 957 ms                                                   | 785 ms: 1.22x faster                                                              |
| generators                       | 21.9 ms                                                  | 18.1 ms: 1.21x faster                                                             |
| json_dumps                       | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                             |
| html5lib                         | 23.0 ms                                                  | 19.4 ms: 1.18x faster                                                             |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                             |
| hexiom                           | 3.04 ms                                                  | 2.57 ms: 1.18x faster                                                             |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                             |
| genshi_text                      | 10.5 ms                                                  | 8.90 ms: 1.18x faster                                                             |
| typing_runtime_protocols         | 71.0 us                                                  | 60.4 us: 1.17x faster                                                             |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                             |
| fannkuch                         | 176 ms                                                   | 150 ms: 1.17x faster                                                              |
| pycparser                        | 497 ms                                                   | 428 ms: 1.16x faster                                                              |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                              |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                             |
| thrift                           | 322 us                                                   | 281 us: 1.15x faster                                                              |
| sphinx                           | 434 ms                                                   | 379 ms: 1.14x faster                                                              |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                             |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                             |
| meteor_contest                   | 47.7 ms                                                  | 43.7 ms: 1.09x faster                                                             |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                             |
| regex_dna                        | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                             |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                              |
| json                             | 1.93 ms                                                  | 1.79 ms: 1.08x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 214 ms: 1.08x faster                                                              |
| 2to3                             | 114 ms                                                   | 107 ms: 1.07x faster                                                              |
| docutils                         | 1.02 sec                                                 | 973 ms: 1.05x faster                                                              |
| sympy_sum                        | 57.6 ms                                                  | 54.9 ms: 1.05x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                              |
| pidigits                         | 161 ms                                                   | 155 ms: 1.04x faster                                                              |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.04x faster                                                             |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                             |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                              |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.02x faster                                                             |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                              |
| gc_traversal                     | 2.01 ms                                                  | 1.98 ms: 1.01x faster                                                             |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                              |
| connected_components             | 201 ms                                                   | 198 ms: 1.01x faster                                                              |
| regex_v8                         | 9.59 ms                                                  | 9.51 ms: 1.01x faster                                                             |
| django_template                  | 13.6 ms                                                  | 13.5 ms: 1.01x faster                                                             |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                              |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                              |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                              |
| create_gc_cycles                 | 830 us                                                   | 890 us: 1.07x slower                                                              |
| python_startup                   | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                             |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                                             |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                              |
| coverage                         | 26.9 ms                                                  | 31.4 ms: 1.17x slower                                                             |
| many_optionals                   | 195 us                                                   | 243 us: 1.24x slower                                                              |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.2 ms: 2.37x slower                                                             |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                                      |
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260102-3.15.0a3+-884a7a7-JIT/bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.273x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.25x