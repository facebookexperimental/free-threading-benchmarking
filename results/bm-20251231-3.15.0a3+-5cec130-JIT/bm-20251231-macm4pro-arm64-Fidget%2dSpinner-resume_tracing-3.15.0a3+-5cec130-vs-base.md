# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 5cec130
- commit date: 2025-12-31
- overall geometric mean: 1.008x slower
- HPT reliability: 96.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 109 ms                                                                   | 111 ms: 1.03x slower                                                         |
| docutils       | 997 ms                                                                   | 1.04 sec: 1.04x slower                                                       |
| sphinx         | 387 ms                                                                   | 410 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg               | 96.8 ms                                                                  | 92.7 ms: 1.04x faster                                                        |
| async_tree_io_tg                 | 218 ms                                                                   | 209 ms: 1.04x faster                                                         |
| async_tree_memoization_tg        | 135 ms                                                                   | 130 ms: 1.03x faster                                                         |
| async_tree_eager_io_tg           | 218 ms                                                                   | 212 ms: 1.03x faster                                                         |
| async_tree_eager_tg              | 80.0 ms                                                                  | 77.9 ms: 1.03x faster                                                        |
| async_tree_none                  | 98.3 ms                                                                  | 96.1 ms: 1.02x faster                                                        |
| async_tree_io                    | 228 ms                                                                   | 223 ms: 1.02x faster                                                         |
| async_tree_memoization           | 137 ms                                                                   | 134 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 251 ms                                                                   | 247 ms: 1.01x faster                                                         |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 244 ms: 1.01x faster                                                         |
| async_generators                 | 182 ms                                                                   | 183 ms: 1.00x slower                                                         |
| coroutines                       | 10.1 ms                                                                  | 10.3 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 220 ms: 1.01x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 241 ms: 1.01x slower                                                         |
| async_tree_eager_memoization     | 106 ms                                                                   | 108 ms: 1.02x slower                                                         |
| async_tree_eager                 | 37.9 ms                                                                  | 39.3 ms: 1.03x slower                                                        |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 39.5 ms                                                                  | 39.4 ms: 1.00x faster                                                        |
| pidigits       | 160 ms                                                                   | 161 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 40.0 ms                                                                  | 39.7 ms: 1.01x faster                                                        |
| regex_dna      | 93.0 ms                                                                  | 94.5 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 62.3 ms                                                                  | 60.7 ms: 1.03x faster                                                        |
| pickle_pure_python   | 111 us                                                                   | 110 us: 1.00x faster                                                         |
| xml_etree_process    | 21.9 ms                                                                  | 22.0 ms: 1.00x slower                                                        |
| unpickle_pure_python | 72.0 us                                                                  | 72.4 us: 1.01x slower                                                        |
| json_dumps           | 3.64 ms                                                                  | 3.67 ms: 1.01x slower                                                        |
| json_loads           | 10.4 us                                                                  | 10.6 us: 1.02x slower                                                        |
| xml_etree_iterparse  | 37.5 ms                                                                  | 38.2 ms: 1.02x slower                                                        |
| xml_etree_generate   | 31.5 ms                                                                  | 33.0 ms: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.32 ms                                                                  | 6.34 ms: 1.00x slower                                                        |
| python_startup         | 8.76 ms                                                                  | 8.79 ms: 1.00x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.00x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.7 ms                                                                  | 13.1 ms: 1.05x faster                                                        |
| mako            | 4.12 ms                                                                  | 4.10 ms: 1.01x faster                                                        |
| genshi_text     | 8.99 ms                                                                  | 9.37 ms: 1.04x slower                                                        |
| genshi_xml      | 21.2 ms                                                                  | 22.5 ms: 1.06x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format                   | 2.30 us                                                                  | 1.97 us: 1.17x faster                                                        |
| logging_simple                   | 2.09 us                                                                  | 1.79 us: 1.17x faster                                                        |
| django_template                  | 13.7 ms                                                                  | 13.1 ms: 1.05x faster                                                        |
| async_tree_none_tg               | 96.8 ms                                                                  | 92.7 ms: 1.04x faster                                                        |
| scimark_sor                      | 42.2 ms                                                                  | 40.4 ms: 1.04x faster                                                        |
| chaos                            | 21.9 ms                                                                  | 21.0 ms: 1.04x faster                                                        |
| async_tree_io_tg                 | 218 ms                                                                   | 209 ms: 1.04x faster                                                         |
| raytrace                         | 106 ms                                                                   | 102 ms: 1.04x faster                                                         |
| coverage                         | 33.3 ms                                                                  | 32.1 ms: 1.04x faster                                                        |
| async_tree_memoization_tg        | 135 ms                                                                   | 130 ms: 1.03x faster                                                         |
| deltablue                        | 1.12 ms                                                                  | 1.09 ms: 1.03x faster                                                        |
| async_tree_eager_io_tg           | 218 ms                                                                   | 212 ms: 1.03x faster                                                         |
| async_tree_eager_tg              | 80.0 ms                                                                  | 77.9 ms: 1.03x faster                                                        |
| go                               | 43.1 ms                                                                  | 42.0 ms: 1.03x faster                                                        |
| xml_etree_parse                  | 62.3 ms                                                                  | 60.7 ms: 1.03x faster                                                        |
| async_tree_none                  | 98.3 ms                                                                  | 96.1 ms: 1.02x faster                                                        |
| async_tree_io                    | 228 ms                                                                   | 223 ms: 1.02x faster                                                         |
| async_tree_memoization           | 137 ms                                                                   | 134 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 251 ms                                                                   | 247 ms: 1.01x faster                                                         |
| scimark_sparse_mat_mult          | 1.93 ms                                                                  | 1.91 ms: 1.01x faster                                                        |
| scimark_fft                      | 102 ms                                                                   | 101 ms: 1.01x faster                                                         |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 244 ms: 1.01x faster                                                         |
| regex_compile                    | 40.0 ms                                                                  | 39.7 ms: 1.01x faster                                                        |
| mako                             | 4.12 ms                                                                  | 4.10 ms: 1.01x faster                                                        |
| nbody                            | 39.5 ms                                                                  | 39.4 ms: 1.00x faster                                                        |
| pickle_pure_python               | 111 us                                                                   | 110 us: 1.00x faster                                                         |
| k_core                           | 865 ms                                                                   | 863 ms: 1.00x faster                                                         |
| python_startup_no_site           | 6.32 ms                                                                  | 6.34 ms: 1.00x slower                                                        |
| async_generators                 | 182 ms                                                                   | 183 ms: 1.00x slower                                                         |
| python_startup                   | 8.76 ms                                                                  | 8.79 ms: 1.00x slower                                                        |
| shortest_path                    | 216 ms                                                                   | 217 ms: 1.00x slower                                                         |
| xml_etree_process                | 21.9 ms                                                                  | 22.0 ms: 1.00x slower                                                        |
| pathlib                          | 10.8 ms                                                                  | 10.8 ms: 1.00x slower                                                        |
| pprint_pformat                   | 528 ms                                                                   | 531 ms: 1.00x slower                                                         |
| unpickle_pure_python             | 72.0 us                                                                  | 72.4 us: 1.01x slower                                                        |
| create_gc_cycles                 | 907 us                                                                   | 914 us: 1.01x slower                                                         |
| pidigits                         | 160 ms                                                                   | 161 ms: 1.01x slower                                                         |
| dulwich_log                      | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                        |
| deepcopy_memo                    | 11.7 us                                                                  | 11.8 us: 1.01x slower                                                        |
| gc_traversal                     | 2.02 ms                                                                  | 2.04 ms: 1.01x slower                                                        |
| json_dumps                       | 3.64 ms                                                                  | 3.67 ms: 1.01x slower                                                        |
| coroutines                       | 10.1 ms                                                                  | 10.3 ms: 1.01x slower                                                        |
| nqueens                          | 38.8 ms                                                                  | 39.2 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 220 ms: 1.01x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 241 ms: 1.01x slower                                                         |
| bench_thread_pool                | 428 us                                                                   | 433 us: 1.01x slower                                                         |
| crypto_pyaes                     | 30.7 ms                                                                  | 31.0 ms: 1.01x slower                                                        |
| pprint_safe_repr                 | 260 ms                                                                   | 263 ms: 1.01x slower                                                         |
| meteor_contest                   | 44.3 ms                                                                  | 44.9 ms: 1.01x slower                                                        |
| spectral_norm                    | 40.6 ms                                                                  | 41.2 ms: 1.01x slower                                                        |
| bench_mp_pool                    | 43.9 ms                                                                  | 44.6 ms: 1.01x slower                                                        |
| json_loads                       | 10.4 us                                                                  | 10.6 us: 1.02x slower                                                        |
| subparsers                       | 3.85 ms                                                                  | 3.92 ms: 1.02x slower                                                        |
| generators                       | 18.8 ms                                                                  | 19.1 ms: 1.02x slower                                                        |
| regex_dna                        | 93.0 ms                                                                  | 94.5 ms: 1.02x slower                                                        |
| bpe_tokeniser                    | 1.83 sec                                                                 | 1.87 sec: 1.02x slower                                                       |
| comprehensions                   | 6.10 us                                                                  | 6.22 us: 1.02x slower                                                        |
| xml_etree_iterparse              | 37.5 ms                                                                  | 38.2 ms: 1.02x slower                                                        |
| logging_silent                   | 33.4 ns                                                                  | 34.2 ns: 1.02x slower                                                        |
| async_tree_eager_memoization     | 106 ms                                                                   | 108 ms: 1.02x slower                                                         |
| 2to3                             | 109 ms                                                                   | 111 ms: 1.03x slower                                                         |
| hexiom                           | 2.58 ms                                                                  | 2.65 ms: 1.03x slower                                                        |
| sympy_expand                     | 174 ms                                                                   | 179 ms: 1.03x slower                                                         |
| sqlglot_v2_parse                 | 466 us                                                                   | 481 us: 1.03x slower                                                         |
| richards_super                   | 11.5 ms                                                                  | 11.9 ms: 1.03x slower                                                        |
| async_tree_eager                 | 37.9 ms                                                                  | 39.3 ms: 1.03x slower                                                        |
| docutils                         | 997 ms                                                                   | 1.04 sec: 1.04x slower                                                       |
| genshi_text                      | 8.99 ms                                                                  | 9.37 ms: 1.04x slower                                                        |
| many_optionals                   | 249 us                                                                   | 259 us: 1.04x slower                                                         |
| xml_etree_generate               | 31.5 ms                                                                  | 33.0 ms: 1.05x slower                                                        |
| deepcopy                         | 97.2 us                                                                  | 102 us: 1.05x slower                                                         |
| pycparser                        | 440 ms                                                                   | 463 ms: 1.05x slower                                                         |
| richards                         | 9.61 ms                                                                  | 10.2 ms: 1.06x slower                                                        |
| sphinx                           | 387 ms                                                                   | 410 ms: 1.06x slower                                                         |
| genshi_xml                       | 21.2 ms                                                                  | 22.5 ms: 1.06x slower                                                        |
| sqlglot_v2_transpile             | 591 us                                                                   | 629 us: 1.06x slower                                                         |
| pylint                           | 121 ms                                                                   | 133 ms: 1.10x slower                                                         |
| sqlglot_v2_normalize             | 47.3 ms                                                                  | 51.9 ms: 1.10x slower                                                        |
| mdp                              | 578 ms                                                                   | 634 ms: 1.10x slower                                                         |
| sympy_sum                        | 55.5 ms                                                                  | 61.2 ms: 1.10x slower                                                        |
| sympy_str                        | 104 ms                                                                   | 115 ms: 1.11x slower                                                         |
| sympy_integrate                  | 7.43 ms                                                                  | 8.33 ms: 1.12x slower                                                        |
| sqlglot_v2_optimize              | 24.3 ms                                                                  | 27.7 ms: 1.14x slower                                                        |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (18): async_tree_eager_memoization_tg, html5lib, scimark_monte_carlo, fannkuch, tomli_loads, connected_components, async_tree_eager_io, sqlite_synth, regex_v8, scimark_lu, pyflate, thrift, typing_runtime_protocols, telco, deepcopy_reduce, regex_effbot, float, json
Ignored benchmarks (1) of results/bm-20251231-3.15.0a3+-5cec130-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 96.44% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x