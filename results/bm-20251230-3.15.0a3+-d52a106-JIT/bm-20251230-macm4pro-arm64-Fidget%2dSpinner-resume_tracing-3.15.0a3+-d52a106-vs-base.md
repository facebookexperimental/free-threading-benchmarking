# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: d52a106
- commit date: 2025-12-30
- overall geometric mean: 1.004x faster
- HPT reliability: 89.20%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 109 ms: 1.01x faster                                                         |
| html5lib       | 20.1 ms                                                                  | 19.8 ms: 1.02x faster                                                        |
| sphinx         | 391 ms                                                                   | 397 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg                 | 224 ms                                                                   | 211 ms: 1.07x faster                                                         |
| async_tree_none_tg               | 98.2 ms                                                                  | 92.4 ms: 1.06x faster                                                        |
| async_tree_eager_io_tg           | 222 ms                                                                   | 210 ms: 1.06x faster                                                         |
| async_tree_memoization_tg        | 136 ms                                                                   | 130 ms: 1.05x faster                                                         |
| async_tree_none                  | 98.9 ms                                                                  | 94.4 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 254 ms                                                                   | 243 ms: 1.04x faster                                                         |
| async_tree_io                    | 231 ms                                                                   | 222 ms: 1.04x faster                                                         |
| async_tree_eager_tg              | 80.7 ms                                                                  | 77.7 ms: 1.04x faster                                                        |
| async_tree_eager_memoization_tg  | 122 ms                                                                   | 118 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed          | 248 ms                                                                   | 240 ms: 1.04x faster                                                         |
| async_tree_memoization           | 137 ms                                                                   | 133 ms: 1.03x faster                                                         |
| async_tree_eager_io              | 221 ms                                                                   | 214 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                   | 216 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 237 ms: 1.01x faster                                                         |
| coroutines                       | 10.2 ms                                                                  | 10.1 ms: 1.01x faster                                                        |
| asyncio_websockets               | 188 ms                                                                   | 187 ms: 1.00x faster                                                         |
| Geometric mean                   | (ref)                                                                    | 1.03x faster                                                                 |

Benchmark hidden because not significant (3): async_generators, async_tree_eager_memoization, async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 39.7 ms                                                                  | 39.9 ms: 1.00x slower                                                        |
| pidigits       | 162 ms                                                                   | 163 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 96.9 ms                                                                  | 95.3 ms: 1.02x faster                                                        |
| regex_effbot   | 1.46 ms                                                                  | 1.44 ms: 1.01x faster                                                        |
| regex_v8       | 9.82 ms                                                                  | 9.77 ms: 1.00x faster                                                        |
| regex_compile  | 40.4 ms                                                                  | 46.4 ms: 1.15x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|---------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse     | 63.9 ms                                                                  | 60.4 ms: 1.06x faster                                                        |
| xml_etree_iterparse | 38.6 ms                                                                  | 37.2 ms: 1.04x faster                                                        |
| tomli_loads         | 796 ms                                                                   | 786 ms: 1.01x faster                                                         |
| json_loads          | 10.6 us                                                                  | 10.5 us: 1.01x faster                                                        |
| pickle_pure_python  | 112 us                                                                   | 111 us: 1.01x faster                                                         |
| json_dumps          | 3.68 ms                                                                  | 3.70 ms: 1.01x slower                                                        |
| xml_etree_process   | 21.9 ms                                                                  | 22.1 ms: 1.01x slower                                                        |
| xml_etree_generate  | 31.4 ms                                                                  | 33.3 ms: 1.06x slower                                                        |
| Geometric mean      | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.81 ms                                                                  | 8.87 ms: 1.01x slower                                                        |
| python_startup_no_site | 6.35 ms                                                                  | 6.40 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.9 ms                                                                  | 12.9 ms: 1.08x faster                                                        |
| mako            | 4.14 ms                                                                  | 4.17 ms: 1.01x slower                                                        |
| genshi_text     | 8.99 ms                                                                  | 9.29 ms: 1.03x slower                                                        |
| genshi_xml      | 21.1 ms                                                                  | 22.2 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.00x slower                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format                   | 2.34 us                                                                  | 2.00 us: 1.17x faster                                                        |
| logging_simple                   | 2.14 us                                                                  | 1.83 us: 1.17x faster                                                        |
| django_template                  | 13.9 ms                                                                  | 12.9 ms: 1.08x faster                                                        |
| async_tree_io_tg                 | 224 ms                                                                   | 211 ms: 1.07x faster                                                         |
| async_tree_none_tg               | 98.2 ms                                                                  | 92.4 ms: 1.06x faster                                                        |
| deltablue                        | 1.13 ms                                                                  | 1.06 ms: 1.06x faster                                                        |
| xml_etree_parse                  | 63.9 ms                                                                  | 60.4 ms: 1.06x faster                                                        |
| async_tree_eager_io_tg           | 222 ms                                                                   | 210 ms: 1.06x faster                                                         |
| coverage                         | 33.8 ms                                                                  | 32.0 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 136 ms                                                                   | 130 ms: 1.05x faster                                                         |
| async_tree_none                  | 98.9 ms                                                                  | 94.4 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 254 ms                                                                   | 243 ms: 1.04x faster                                                         |
| scimark_sor                      | 42.3 ms                                                                  | 40.5 ms: 1.04x faster                                                        |
| async_tree_io                    | 231 ms                                                                   | 222 ms: 1.04x faster                                                         |
| async_tree_eager_tg              | 80.7 ms                                                                  | 77.7 ms: 1.04x faster                                                        |
| xml_etree_iterparse              | 38.6 ms                                                                  | 37.2 ms: 1.04x faster                                                        |
| async_tree_eager_memoization_tg  | 122 ms                                                                   | 118 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed          | 248 ms                                                                   | 240 ms: 1.04x faster                                                         |
| chaos                            | 22.1 ms                                                                  | 21.4 ms: 1.03x faster                                                        |
| async_tree_memoization           | 137 ms                                                                   | 133 ms: 1.03x faster                                                         |
| async_tree_eager_io              | 221 ms                                                                   | 214 ms: 1.03x faster                                                         |
| richards                         | 9.75 ms                                                                  | 9.51 ms: 1.02x faster                                                        |
| raytrace                         | 106 ms                                                                   | 104 ms: 1.02x faster                                                         |
| many_optionals                   | 254 us                                                                   | 249 us: 1.02x faster                                                         |
| fannkuch                         | 154 ms                                                                   | 151 ms: 1.02x faster                                                         |
| subparsers                       | 3.92 ms                                                                  | 3.85 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                   | 216 ms: 1.02x faster                                                         |
| html5lib                         | 20.1 ms                                                                  | 19.8 ms: 1.02x faster                                                        |
| regex_dna                        | 96.9 ms                                                                  | 95.3 ms: 1.02x faster                                                        |
| tomli_loads                      | 796 ms                                                                   | 786 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 237 ms: 1.01x faster                                                         |
| coroutines                       | 10.2 ms                                                                  | 10.1 ms: 1.01x faster                                                        |
| 2to3                             | 110 ms                                                                   | 109 ms: 1.01x faster                                                         |
| telco                            | 2.61 ms                                                                  | 2.58 ms: 1.01x faster                                                        |
| regex_effbot                     | 1.46 ms                                                                  | 1.44 ms: 1.01x faster                                                        |
| sqlite_synth                     | 974 ns                                                                   | 965 ns: 1.01x faster                                                         |
| deepcopy_memo                    | 11.8 us                                                                  | 11.7 us: 1.01x faster                                                        |
| json_loads                       | 10.6 us                                                                  | 10.5 us: 1.01x faster                                                        |
| pickle_pure_python               | 112 us                                                                   | 111 us: 1.01x faster                                                         |
| thrift                           | 290 us                                                                   | 288 us: 1.01x faster                                                         |
| regex_v8                         | 9.82 ms                                                                  | 9.77 ms: 1.00x faster                                                        |
| asyncio_websockets               | 188 ms                                                                   | 187 ms: 1.00x faster                                                         |
| bench_mp_pool                    | 44.7 ms                                                                  | 44.5 ms: 1.00x faster                                                        |
| gc_traversal                     | 2.06 ms                                                                  | 2.05 ms: 1.00x faster                                                        |
| create_gc_cycles                 | 919 us                                                                   | 915 us: 1.00x faster                                                         |
| scimark_fft                      | 102 ms                                                                   | 101 ms: 1.00x faster                                                         |
| scimark_monte_carlo              | 22.7 ms                                                                  | 22.6 ms: 1.00x faster                                                        |
| scimark_lu                       | 36.7 ms                                                                  | 36.5 ms: 1.00x faster                                                        |
| crypto_pyaes                     | 31.1 ms                                                                  | 31.3 ms: 1.00x slower                                                        |
| nbody                            | 39.7 ms                                                                  | 39.9 ms: 1.00x slower                                                        |
| shortest_path                    | 215 ms                                                                   | 216 ms: 1.00x slower                                                         |
| json_dumps                       | 3.68 ms                                                                  | 3.70 ms: 1.01x slower                                                        |
| xml_etree_process                | 21.9 ms                                                                  | 22.1 ms: 1.01x slower                                                        |
| connected_components             | 197 ms                                                                   | 198 ms: 1.01x slower                                                         |
| pprint_pformat                   | 529 ms                                                                   | 532 ms: 1.01x slower                                                         |
| pathlib                          | 10.8 ms                                                                  | 10.9 ms: 1.01x slower                                                        |
| python_startup                   | 8.81 ms                                                                  | 8.87 ms: 1.01x slower                                                        |
| python_startup_no_site           | 6.35 ms                                                                  | 6.40 ms: 1.01x slower                                                        |
| spectral_norm                    | 41.1 ms                                                                  | 41.4 ms: 1.01x slower                                                        |
| pidigits                         | 162 ms                                                                   | 163 ms: 1.01x slower                                                         |
| json                             | 1.85 ms                                                                  | 1.87 ms: 1.01x slower                                                        |
| bpe_tokeniser                    | 1.85 sec                                                                 | 1.87 sec: 1.01x slower                                                       |
| mako                             | 4.14 ms                                                                  | 4.17 ms: 1.01x slower                                                        |
| bench_thread_pool                | 429 us                                                                   | 433 us: 1.01x slower                                                         |
| nqueens                          | 38.8 ms                                                                  | 39.4 ms: 1.01x slower                                                        |
| sphinx                           | 391 ms                                                                   | 397 ms: 1.01x slower                                                         |
| pprint_safe_repr                 | 259 ms                                                                   | 265 ms: 1.02x slower                                                         |
| deepcopy                         | 99.1 us                                                                  | 101 us: 1.02x slower                                                         |
| pyflate                          | 143 ms                                                                   | 147 ms: 1.03x slower                                                         |
| logging_silent                   | 33.2 ns                                                                  | 34.3 ns: 1.03x slower                                                        |
| genshi_text                      | 8.99 ms                                                                  | 9.29 ms: 1.03x slower                                                        |
| sqlglot_v2_parse                 | 471 us                                                                   | 489 us: 1.04x slower                                                         |
| hexiom                           | 2.61 ms                                                                  | 2.73 ms: 1.04x slower                                                        |
| generators                       | 18.9 ms                                                                  | 19.8 ms: 1.05x slower                                                        |
| go                               | 42.7 ms                                                                  | 44.9 ms: 1.05x slower                                                        |
| genshi_xml                       | 21.1 ms                                                                  | 22.2 ms: 1.05x slower                                                        |
| pycparser                        | 444 ms                                                                   | 467 ms: 1.05x slower                                                         |
| xml_etree_generate               | 31.4 ms                                                                  | 33.3 ms: 1.06x slower                                                        |
| mdp                              | 578 ms                                                                   | 641 ms: 1.11x slower                                                         |
| sqlglot_v2_optimize              | 24.6 ms                                                                  | 28.2 ms: 1.14x slower                                                        |
| regex_compile                    | 40.4 ms                                                                  | 46.4 ms: 1.15x slower                                                        |
| comprehensions                   | 6.18 us                                                                  | 7.69 us: 1.24x slower                                                        |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                                 |

Benchmark hidden because not significant (12): typing_runtime_protocols, dulwich_log, async_generators, async_tree_eager_memoization, richards_super, float, unpickle_pure_python, k_core, scimark_sparse_mat_mult, deepcopy_reduce, async_tree_eager, meteor_contest
Ignored benchmarks (8) of results/bm-20251229-3.15.0a3+-6cb245d-JIT/bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d.json: docutils, pylint, sqlglot_v2_normalize, sqlglot_v2_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 89.20% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x