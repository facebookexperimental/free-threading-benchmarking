# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 564677c
- commit date: 2025-12-31
- overall geometric mean: 1.004x slower
- HPT reliability: 77.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 109 ms                                                                   | 109 ms: 1.01x slower                                                         |
| docutils       | 997 ms                                                                   | 1.02 sec: 1.02x slower                                                       |
| html5lib       | 19.8 ms                                                                  | 19.5 ms: 1.02x faster                                                        |
| sphinx         | 387 ms                                                                   | 400 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|---------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg              | 96.8 ms                                                                  | 92.7 ms: 1.04x faster                                                        |
| async_tree_io_tg                | 218 ms                                                                   | 209 ms: 1.04x faster                                                         |
| async_tree_none                 | 98.3 ms                                                                  | 94.5 ms: 1.04x faster                                                        |
| async_tree_eager_io_tg          | 218 ms                                                                   | 210 ms: 1.04x faster                                                         |
| async_tree_io                   | 228 ms                                                                   | 220 ms: 1.04x faster                                                         |
| async_tree_memoization_tg       | 135 ms                                                                   | 130 ms: 1.04x faster                                                         |
| async_tree_eager_tg             | 80.0 ms                                                                  | 77.3 ms: 1.04x faster                                                        |
| async_tree_memoization          | 137 ms                                                                   | 132 ms: 1.03x faster                                                         |
| async_tree_eager_io             | 217 ms                                                                   | 211 ms: 1.03x faster                                                         |
| async_tree_eager_memoization_tg | 120 ms                                                                   | 117 ms: 1.03x faster                                                         |
| coroutines                      | 10.1 ms                                                                  | 9.93 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed         | 246 ms                                                                   | 242 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg      | 251 ms                                                                   | 246 ms: 1.02x faster                                                         |
| async_generators                | 182 ms                                                                   | 183 ms: 1.00x slower                                                         |
| async_tree_eager                | 37.9 ms                                                                  | 38.2 ms: 1.01x slower                                                        |
| Geometric mean                  | (ref)                                                                    | 1.02x faster                                                                 |

Benchmark hidden because not significant (3): async_tree_eager_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 160 ms                                                                   | 161 ms: 1.01x slower                                                         |
| nbody          | 39.5 ms                                                                  | 40.0 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 9.60 ms                                                                  | 9.47 ms: 1.01x faster                                                        |
| regex_compile  | 40.0 ms                                                                  | 39.8 ms: 1.00x faster                                                        |
| regex_effbot   | 1.43 ms                                                                  | 1.44 ms: 1.01x slower                                                        |
| regex_dna      | 93.0 ms                                                                  | 94.4 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 62.3 ms                                                                  | 58.9 ms: 1.06x faster                                                        |
| xml_etree_iterparse  | 37.5 ms                                                                  | 37.0 ms: 1.01x faster                                                        |
| tomli_loads          | 794 ms                                                                   | 784 ms: 1.01x faster                                                         |
| unpickle_pure_python | 72.0 us                                                                  | 72.6 us: 1.01x slower                                                        |
| pickle_pure_python   | 111 us                                                                   | 112 us: 1.01x slower                                                         |
| xml_etree_process    | 21.9 ms                                                                  | 22.3 ms: 1.02x slower                                                        |
| xml_etree_generate   | 31.5 ms                                                                  | 33.4 ms: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): json_dumps, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.32 ms                                                                  | 6.33 ms: 1.00x slower                                                        |
| python_startup         | 8.76 ms                                                                  | 8.78 ms: 1.00x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.00x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.7 ms                                                                  | 13.0 ms: 1.05x faster                                                        |
| genshi_text     | 8.99 ms                                                                  | 9.14 ms: 1.02x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|---------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse                 | 62.3 ms                                                                  | 58.9 ms: 1.06x faster                                                        |
| django_template                 | 13.7 ms                                                                  | 13.0 ms: 1.05x faster                                                        |
| chaos                           | 21.9 ms                                                                  | 20.8 ms: 1.05x faster                                                        |
| async_tree_none_tg              | 96.8 ms                                                                  | 92.7 ms: 1.04x faster                                                        |
| scimark_sor                     | 42.2 ms                                                                  | 40.5 ms: 1.04x faster                                                        |
| logging_simple                  | 2.09 us                                                                  | 2.01 us: 1.04x faster                                                        |
| async_tree_io_tg                | 218 ms                                                                   | 209 ms: 1.04x faster                                                         |
| async_tree_none                 | 98.3 ms                                                                  | 94.5 ms: 1.04x faster                                                        |
| deltablue                       | 1.12 ms                                                                  | 1.08 ms: 1.04x faster                                                        |
| async_tree_eager_io_tg          | 218 ms                                                                   | 210 ms: 1.04x faster                                                         |
| async_tree_io                   | 228 ms                                                                   | 220 ms: 1.04x faster                                                         |
| async_tree_memoization_tg       | 135 ms                                                                   | 130 ms: 1.04x faster                                                         |
| async_tree_eager_tg             | 80.0 ms                                                                  | 77.3 ms: 1.04x faster                                                        |
| async_tree_memoization          | 137 ms                                                                   | 132 ms: 1.03x faster                                                         |
| logging_format                  | 2.30 us                                                                  | 2.23 us: 1.03x faster                                                        |
| raytrace                        | 106 ms                                                                   | 102 ms: 1.03x faster                                                         |
| async_tree_eager_io             | 217 ms                                                                   | 211 ms: 1.03x faster                                                         |
| coverage                        | 33.3 ms                                                                  | 32.4 ms: 1.03x faster                                                        |
| async_tree_eager_memoization_tg | 120 ms                                                                   | 117 ms: 1.03x faster                                                         |
| coroutines                      | 10.1 ms                                                                  | 9.93 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed         | 246 ms                                                                   | 242 ms: 1.02x faster                                                         |
| richards                        | 9.61 ms                                                                  | 9.43 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed_tg      | 251 ms                                                                   | 246 ms: 1.02x faster                                                         |
| html5lib                        | 19.8 ms                                                                  | 19.5 ms: 1.02x faster                                                        |
| xml_etree_iterparse             | 37.5 ms                                                                  | 37.0 ms: 1.01x faster                                                        |
| regex_v8                        | 9.60 ms                                                                  | 9.47 ms: 1.01x faster                                                        |
| tomli_loads                     | 794 ms                                                                   | 784 ms: 1.01x faster                                                         |
| scimark_monte_carlo             | 22.5 ms                                                                  | 22.3 ms: 1.01x faster                                                        |
| json                            | 1.84 ms                                                                  | 1.82 ms: 1.01x faster                                                        |
| fannkuch                        | 153 ms                                                                   | 152 ms: 1.01x faster                                                         |
| regex_compile                   | 40.0 ms                                                                  | 39.8 ms: 1.00x faster                                                        |
| scimark_fft                     | 102 ms                                                                   | 101 ms: 1.00x faster                                                         |
| connected_components            | 198 ms                                                                   | 197 ms: 1.00x faster                                                         |
| python_startup_no_site          | 6.32 ms                                                                  | 6.33 ms: 1.00x slower                                                        |
| python_startup                  | 8.76 ms                                                                  | 8.78 ms: 1.00x slower                                                        |
| shortest_path                   | 216 ms                                                                   | 216 ms: 1.00x slower                                                         |
| async_generators                | 182 ms                                                                   | 183 ms: 1.00x slower                                                         |
| gc_traversal                    | 2.02 ms                                                                  | 2.03 ms: 1.00x slower                                                        |
| bench_mp_pool                   | 43.9 ms                                                                  | 44.1 ms: 1.00x slower                                                        |
| logging_silent                  | 33.4 ns                                                                  | 33.6 ns: 1.00x slower                                                        |
| regex_effbot                    | 1.43 ms                                                                  | 1.44 ms: 1.01x slower                                                        |
| crypto_pyaes                    | 30.7 ms                                                                  | 30.9 ms: 1.01x slower                                                        |
| pidigits                        | 160 ms                                                                   | 161 ms: 1.01x slower                                                         |
| async_tree_eager                | 37.9 ms                                                                  | 38.2 ms: 1.01x slower                                                        |
| 2to3                            | 109 ms                                                                   | 109 ms: 1.01x slower                                                         |
| unpickle_pure_python            | 72.0 us                                                                  | 72.6 us: 1.01x slower                                                        |
| pathlib                         | 10.8 ms                                                                  | 10.9 ms: 1.01x slower                                                        |
| typing_runtime_protocols        | 62.1 us                                                                  | 62.8 us: 1.01x slower                                                        |
| deepcopy                        | 97.2 us                                                                  | 98.4 us: 1.01x slower                                                        |
| nbody                           | 39.5 ms                                                                  | 40.0 ms: 1.01x slower                                                        |
| pickle_pure_python              | 111 us                                                                   | 112 us: 1.01x slower                                                         |
| pprint_safe_repr                | 260 ms                                                                   | 263 ms: 1.01x slower                                                         |
| bench_thread_pool               | 428 us                                                                   | 434 us: 1.01x slower                                                         |
| many_optionals                  | 249 us                                                                   | 252 us: 1.01x slower                                                         |
| bpe_tokeniser                   | 1.83 sec                                                                 | 1.86 sec: 1.02x slower                                                       |
| regex_dna                       | 93.0 ms                                                                  | 94.4 ms: 1.02x slower                                                        |
| thrift                          | 286 us                                                                   | 291 us: 1.02x slower                                                         |
| genshi_text                     | 8.99 ms                                                                  | 9.14 ms: 1.02x slower                                                        |
| scimark_lu                      | 36.4 ms                                                                  | 37.0 ms: 1.02x slower                                                        |
| nqueens                         | 38.8 ms                                                                  | 39.4 ms: 1.02x slower                                                        |
| comprehensions                  | 6.10 us                                                                  | 6.21 us: 1.02x slower                                                        |
| xml_etree_process               | 21.9 ms                                                                  | 22.3 ms: 1.02x slower                                                        |
| meteor_contest                  | 44.3 ms                                                                  | 45.2 ms: 1.02x slower                                                        |
| docutils                        | 997 ms                                                                   | 1.02 sec: 1.02x slower                                                       |
| go                              | 43.1 ms                                                                  | 44.2 ms: 1.02x slower                                                        |
| sqlglot_v2_parse                | 466 us                                                                   | 480 us: 1.03x slower                                                         |
| sympy_expand                    | 174 ms                                                                   | 179 ms: 1.03x slower                                                         |
| sphinx                          | 387 ms                                                                   | 400 ms: 1.03x slower                                                         |
| pycparser                       | 440 ms                                                                   | 458 ms: 1.04x slower                                                         |
| sqlglot_v2_transpile            | 591 us                                                                   | 618 us: 1.05x slower                                                         |
| hexiom                          | 2.58 ms                                                                  | 2.72 ms: 1.05x slower                                                        |
| generators                      | 18.8 ms                                                                  | 19.7 ms: 1.05x slower                                                        |
| sqlglot_v2_normalize            | 47.3 ms                                                                  | 50.1 ms: 1.06x slower                                                        |
| xml_etree_generate              | 31.5 ms                                                                  | 33.4 ms: 1.06x slower                                                        |
| sympy_str                       | 104 ms                                                                   | 114 ms: 1.09x slower                                                         |
| sympy_sum                       | 55.5 ms                                                                  | 61.0 ms: 1.10x slower                                                        |
| sympy_integrate                 | 7.43 ms                                                                  | 8.22 ms: 1.11x slower                                                        |
| mdp                             | 578 ms                                                                   | 648 ms: 1.12x slower                                                         |
| sqlglot_v2_optimize             | 24.3 ms                                                                  | 29.3 ms: 1.20x slower                                                        |
| Geometric mean                  | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (22): richards_super, deepcopy_reduce, dulwich_log, mako, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed, deepcopy_memo, k_core, sqlite_synth, spectral_norm, subparsers, telco, pprint_pformat, json_dumps, json_loads, genshi_xml, async_tree_eager_memoization, scimark_sparse_mat_mult, float, create_gc_cycles, pyflate, pylint
Ignored benchmarks (1) of results/bm-20251231-3.15.0a3+-564677c-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 77.56% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x