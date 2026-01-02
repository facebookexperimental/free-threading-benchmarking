# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: call_function_ex_py
- machine: darwin-arm64
- commit hash: 884a7a7
- commit date: 2026-01-02
- overall geometric mean: 1.180x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 107 ms: 1.05x faster                                                              |
| docutils       | 1.05 sec                                                       | 973 ms: 1.08x faster                                                              |
| html5lib       | 23.1 ms                                                        | 19.4 ms: 1.19x faster                                                             |
| sphinx         | 409 ms                                                         | 379 ms: 1.08x faster                                                              |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 212 ms: 2.48x faster                                                              |
| async_tree_eager_io_tg           | 521 ms                                                         | 213 ms: 2.45x faster                                                              |
| async_tree_io_tg                 | 405 ms                                                         | 215 ms: 1.88x faster                                                              |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                              |
| async_tree_none                  | 142 ms                                                         | 94.5 ms: 1.51x faster                                                             |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                              |
| async_tree_none_tg               | 133 ms                                                         | 94.7 ms: 1.40x faster                                                             |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.38x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                              |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                              |
| async_tree_eager                 | 43.2 ms                                                        | 35.9 ms: 1.20x faster                                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                              |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                              |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                             |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 214 ms: 1.05x faster                                                              |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                              |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                              |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.2 ms: 2.64x slower                                                             |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.8 ms: 1.38x faster                                                             |
| nbody          | 42.5 ms                                                        | 39.0 ms: 1.09x faster                                                             |
| pidigits       | 166 ms                                                         | 155 ms: 1.07x faster                                                              |
| Geometric mean | (ref)                                                          | 1.17x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.1 ms: 1.23x faster                                                             |
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                             |
| regex_v8       | 10.7 ms                                                        | 9.51 ms: 1.12x faster                                                             |
| regex_dna      | 94.6 ms                                                        | 91.6 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                          | 1.13x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 70.5 us: 1.41x faster                                                             |
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                             |
| tomli_loads          | 1000 ms                                                        | 785 ms: 1.27x faster                                                              |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                             |
| xml_etree_process    | 25.4 ms                                                        | 21.4 ms: 1.19x faster                                                             |
| xml_etree_generate   | 35.8 ms                                                        | 30.2 ms: 1.18x faster                                                             |
| pickle_pure_python   | 130 us                                                         | 110 us: 1.18x faster                                                              |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                             |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                             |
| Geometric mean       | (ref)                                                          | 1.20x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                             |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                             |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.86 ms: 1.14x faster                                                             |
| genshi_text     | 9.97 ms                                                        | 8.90 ms: 1.12x faster                                                             |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                             |
| django_template | 12.5 ms                                                        | 13.5 ms: 1.08x slower                                                             |
| Geometric mean  | (ref)                                                          | 1.04x faster                                                                      |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 212 ms: 2.48x faster                                                              |
| async_tree_eager_io_tg           | 521 ms                                                         | 213 ms: 2.45x faster                                                              |
| richards                         | 22.1 ms                                                        | 9.66 ms: 2.28x faster                                                             |
| richards_super                   | 24.7 ms                                                        | 11.4 ms: 2.16x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 215 ms: 1.88x faster                                                              |
| mdp                              | 1.06 sec                                                       | 567 ms: 1.87x faster                                                              |
| go                               | 72.6 ms                                                        | 41.4 ms: 1.75x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                              |
| k_core                           | 1.46 sec                                                       | 861 ms: 1.70x faster                                                              |
| subparsers                       | 6.26 ms                                                        | 3.79 ms: 1.65x faster                                                             |
| pyflate                          | 222 ms                                                         | 142 ms: 1.56x faster                                                              |
| scimark_sor                      | 64.0 ms                                                        | 41.7 ms: 1.53x faster                                                             |
| deepcopy                         | 145 us                                                         | 95.3 us: 1.52x faster                                                             |
| async_tree_none                  | 142 ms                                                         | 94.5 ms: 1.51x faster                                                             |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                             |
| unpickle_pure_python             | 99.5 us                                                        | 70.5 us: 1.41x faster                                                             |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                              |
| async_tree_none_tg               | 133 ms                                                         | 94.7 ms: 1.40x faster                                                             |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.38x faster                                                              |
| float                            | 31.4 ms                                                        | 22.8 ms: 1.38x faster                                                             |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.1 ms: 1.35x faster                                                             |
| deltablue                        | 1.45 ms                                                        | 1.10 ms: 1.32x faster                                                             |
| deepcopy_reduce                  | 1.30 us                                                        | 991 ns: 1.31x faster                                                              |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                             |
| tomli_loads                      | 1000 ms                                                        | 785 ms: 1.27x faster                                                              |
| pprint_safe_repr                 | 322 ms                                                         | 256 ms: 1.26x faster                                                              |
| scimark_fft                      | 124 ms                                                         | 99.4 ms: 1.24x faster                                                             |
| pprint_pformat                   | 650 ms                                                         | 525 ms: 1.24x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                              |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                              |
| regex_compile                    | 47.9 ms                                                        | 39.1 ms: 1.23x faster                                                             |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                             |
| async_tree_eager                 | 43.2 ms                                                        | 35.9 ms: 1.20x faster                                                             |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                             |
| html5lib                         | 23.1 ms                                                        | 19.4 ms: 1.19x faster                                                             |
| fannkuch                         | 179 ms                                                         | 150 ms: 1.19x faster                                                              |
| scimark_lu                       | 42.8 ms                                                        | 36.0 ms: 1.19x faster                                                             |
| xml_etree_process                | 25.4 ms                                                        | 21.4 ms: 1.19x faster                                                             |
| xml_etree_generate               | 35.8 ms                                                        | 30.2 ms: 1.18x faster                                                             |
| logging_silent                   | 40.6 ns                                                        | 34.3 ns: 1.18x faster                                                             |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.80 sec: 1.18x faster                                                            |
| pickle_pure_python               | 130 us                                                         | 110 us: 1.18x faster                                                              |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                              |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                             |
| mako                             | 4.41 ms                                                        | 3.86 ms: 1.14x faster                                                             |
| chaos                            | 24.3 ms                                                        | 21.5 ms: 1.13x faster                                                             |
| regex_v8                         | 10.7 ms                                                        | 9.51 ms: 1.12x faster                                                             |
| comprehensions                   | 6.80 us                                                        | 6.06 us: 1.12x faster                                                             |
| genshi_text                      | 9.97 ms                                                        | 8.90 ms: 1.12x faster                                                             |
| create_gc_cycles                 | 993 us                                                         | 890 us: 1.12x faster                                                              |
| crypto_pyaes                     | 33.6 ms                                                        | 30.2 ms: 1.11x faster                                                             |
| hexiom                           | 2.85 ms                                                        | 2.57 ms: 1.11x faster                                                             |
| thrift                           | 309 us                                                         | 281 us: 1.10x faster                                                              |
| pycparser                        | 470 ms                                                         | 428 ms: 1.10x faster                                                              |
| meteor_contest                   | 47.9 ms                                                        | 43.7 ms: 1.10x faster                                                             |
| logging_simple                   | 2.24 us                                                        | 2.04 us: 1.10x faster                                                             |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                             |
| nbody                            | 42.5 ms                                                        | 39.0 ms: 1.09x faster                                                             |
| json                             | 1.94 ms                                                        | 1.79 ms: 1.09x faster                                                             |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                              |
| logging_format                   | 2.45 us                                                        | 2.26 us: 1.08x faster                                                             |
| sphinx                           | 409 ms                                                         | 379 ms: 1.08x faster                                                              |
| docutils                         | 1.05 sec                                                       | 973 ms: 1.08x faster                                                              |
| typing_runtime_protocols         | 64.6 us                                                        | 60.4 us: 1.07x faster                                                             |
| pidigits                         | 166 ms                                                         | 155 ms: 1.07x faster                                                              |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                             |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                             |
| spectral_norm                    | 43.7 ms                                                        | 41.3 ms: 1.06x faster                                                             |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                             |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 214 ms: 1.05x faster                                                              |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                              |
| 2to3                             | 112 ms                                                         | 107 ms: 1.05x faster                                                              |
| raytrace                         | 109 ms                                                         | 104 ms: 1.05x faster                                                              |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                              |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                             |
| regex_dna                        | 94.6 ms                                                        | 91.6 ms: 1.03x faster                                                             |
| gc_traversal                     | 2.04 ms                                                        | 1.98 ms: 1.03x faster                                                             |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                             |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                             |
| coverage                         | 31.2 ms                                                        | 31.4 ms: 1.01x slower                                                             |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                             |
| nqueens                          | 37.2 ms                                                        | 38.1 ms: 1.02x slower                                                             |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                              |
| sympy_sum                        | 52.3 ms                                                        | 54.9 ms: 1.05x slower                                                             |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                             |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                              |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                             |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                              |
| django_template                  | 12.5 ms                                                        | 13.5 ms: 1.08x slower                                                             |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                              |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                              |
| generators                       | 15.7 ms                                                        | 18.1 ms: 1.15x slower                                                             |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.15x slower                                                             |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                              |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.2 ms: 2.64x slower                                                             |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                                      |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260102-3.15.0a3+-884a7a7-JIT/bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.180x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.20x