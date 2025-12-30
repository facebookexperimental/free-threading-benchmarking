# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: d84384d
- commit date: 2025-12-30
- overall geometric mean: 1.014x slower
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 113 ms: 1.03x slower                                                         |
| docutils       | 1.01 sec                                                                 | 1.05 sec: 1.03x slower                                                       |
| html5lib       | 20.1 ms                                                                  | 20.6 ms: 1.03x slower                                                        |
| sphinx         | 391 ms                                                                   | 404 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|---------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| coroutines                      | 10.2 ms                                                                  | 9.57 ms: 1.07x faster                                                        |
| async_tree_io_tg                | 224 ms                                                                   | 211 ms: 1.06x faster                                                         |
| async_tree_none_tg              | 98.2 ms                                                                  | 93.7 ms: 1.05x faster                                                        |
| async_tree_eager_io_tg          | 222 ms                                                                   | 213 ms: 1.04x faster                                                         |
| async_tree_memoization_tg       | 136 ms                                                                   | 131 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg | 122 ms                                                                   | 118 ms: 1.03x faster                                                         |
| async_tree_eager_tg             | 80.7 ms                                                                  | 78.6 ms: 1.03x faster                                                        |
| async_tree_eager_io             | 221 ms                                                                   | 216 ms: 1.02x faster                                                         |
| async_tree_io                   | 231 ms                                                                   | 226 ms: 1.02x faster                                                         |
| async_tree_memoization          | 137 ms                                                                   | 134 ms: 1.02x faster                                                         |
| async_tree_none                 | 98.9 ms                                                                  | 96.8 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed_tg      | 254 ms                                                                   | 250 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed         | 248 ms                                                                   | 246 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed   | 220 ms                                                                   | 222 ms: 1.01x slower                                                         |
| asyncio_websockets              | 188 ms                                                                   | 189 ms: 1.01x slower                                                         |
| async_generators                | 184 ms                                                                   | 186 ms: 1.01x slower                                                         |
| async_tree_eager_memoization    | 107 ms                                                                   | 108 ms: 1.01x slower                                                         |
| async_tree_eager                | 38.5 ms                                                                  | 39.0 ms: 1.01x slower                                                        |
| Geometric mean                  | (ref)                                                                    | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 162 ms                                                                   | 167 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 9.82 ms                                                                  | 9.79 ms: 1.00x faster                                                        |
| regex_compile  | 40.4 ms                                                                  | 46.6 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x slower                                                                 |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 38.6 ms                                                                  | 37.1 ms: 1.04x faster                                                        |
| pickle_pure_python   | 112 us                                                                   | 111 us: 1.01x faster                                                         |
| xml_etree_parse      | 63.9 ms                                                                  | 63.4 ms: 1.01x faster                                                        |
| unpickle_pure_python | 72.5 us                                                                  | 72.7 us: 1.00x slower                                                        |
| json_loads           | 10.6 us                                                                  | 10.7 us: 1.01x slower                                                        |
| tomli_loads          | 796 ms                                                                   | 806 ms: 1.01x slower                                                         |
| xml_etree_process    | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                        |
| xml_etree_generate   | 31.4 ms                                                                  | 33.3 ms: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.35 ms                                                                  | 6.51 ms: 1.03x slower                                                        |
| python_startup         | 8.81 ms                                                                  | 9.06 ms: 1.03x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.9 ms                                                                  | 13.1 ms: 1.06x faster                                                        |
| mako            | 4.14 ms                                                                  | 4.16 ms: 1.01x slower                                                        |
| genshi_text     | 8.99 ms                                                                  | 9.36 ms: 1.04x slower                                                        |
| genshi_xml      | 21.1 ms                                                                  | 22.5 ms: 1.06x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|---------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format                  | 2.34 us                                                                  | 1.98 us: 1.18x faster                                                        |
| logging_simple                  | 2.14 us                                                                  | 1.82 us: 1.18x faster                                                        |
| coroutines                      | 10.2 ms                                                                  | 9.57 ms: 1.07x faster                                                        |
| async_tree_io_tg                | 224 ms                                                                   | 211 ms: 1.06x faster                                                         |
| django_template                 | 13.9 ms                                                                  | 13.1 ms: 1.06x faster                                                        |
| scimark_sor                     | 42.3 ms                                                                  | 40.0 ms: 1.06x faster                                                        |
| deltablue                       | 1.13 ms                                                                  | 1.07 ms: 1.05x faster                                                        |
| async_tree_none_tg              | 98.2 ms                                                                  | 93.7 ms: 1.05x faster                                                        |
| async_tree_eager_io_tg          | 222 ms                                                                   | 213 ms: 1.04x faster                                                         |
| xml_etree_iterparse             | 38.6 ms                                                                  | 37.1 ms: 1.04x faster                                                        |
| async_tree_memoization_tg       | 136 ms                                                                   | 131 ms: 1.04x faster                                                         |
| deepcopy_memo                   | 11.8 us                                                                  | 11.4 us: 1.03x faster                                                        |
| coverage                        | 33.8 ms                                                                  | 32.7 ms: 1.03x faster                                                        |
| async_tree_eager_memoization_tg | 122 ms                                                                   | 118 ms: 1.03x faster                                                         |
| raytrace                        | 106 ms                                                                   | 103 ms: 1.03x faster                                                         |
| async_tree_eager_tg             | 80.7 ms                                                                  | 78.6 ms: 1.03x faster                                                        |
| chaos                           | 22.1 ms                                                                  | 21.6 ms: 1.03x faster                                                        |
| async_tree_eager_io             | 221 ms                                                                   | 216 ms: 1.02x faster                                                         |
| async_tree_io                   | 231 ms                                                                   | 226 ms: 1.02x faster                                                         |
| async_tree_memoization          | 137 ms                                                                   | 134 ms: 1.02x faster                                                         |
| async_tree_none                 | 98.9 ms                                                                  | 96.8 ms: 1.02x faster                                                        |
| deepcopy_reduce                 | 1.03 us                                                                  | 1.01 us: 1.02x faster                                                        |
| sqlglot_v2_parse                | 471 us                                                                   | 464 us: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg      | 254 ms                                                                   | 250 ms: 1.02x faster                                                         |
| typing_runtime_protocols        | 62.9 us                                                                  | 62.0 us: 1.01x faster                                                        |
| telco                           | 2.61 ms                                                                  | 2.57 ms: 1.01x faster                                                        |
| pickle_pure_python              | 112 us                                                                   | 111 us: 1.01x faster                                                         |
| thrift                          | 290 us                                                                   | 287 us: 1.01x faster                                                         |
| async_tree_cpu_io_mixed         | 248 ms                                                                   | 246 ms: 1.01x faster                                                         |
| xml_etree_parse                 | 63.9 ms                                                                  | 63.4 ms: 1.01x faster                                                        |
| regex_v8                        | 9.82 ms                                                                  | 9.79 ms: 1.00x faster                                                        |
| unpickle_pure_python            | 72.5 us                                                                  | 72.7 us: 1.00x slower                                                        |
| subparsers                      | 3.92 ms                                                                  | 3.93 ms: 1.00x slower                                                        |
| crypto_pyaes                    | 31.1 ms                                                                  | 31.3 ms: 1.00x slower                                                        |
| scimark_lu                      | 36.7 ms                                                                  | 36.8 ms: 1.01x slower                                                        |
| k_core                          | 864 ms                                                                   | 869 ms: 1.01x slower                                                         |
| connected_components            | 197 ms                                                                   | 198 ms: 1.01x slower                                                         |
| mako                            | 4.14 ms                                                                  | 4.16 ms: 1.01x slower                                                        |
| dulwich_log                     | 18.7 ms                                                                  | 18.8 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed   | 220 ms                                                                   | 222 ms: 1.01x slower                                                         |
| asyncio_websockets              | 188 ms                                                                   | 189 ms: 1.01x slower                                                         |
| async_generators                | 184 ms                                                                   | 186 ms: 1.01x slower                                                         |
| shortest_path                   | 215 ms                                                                   | 217 ms: 1.01x slower                                                         |
| scimark_fft                     | 102 ms                                                                   | 103 ms: 1.01x slower                                                         |
| async_tree_eager_memoization    | 107 ms                                                                   | 108 ms: 1.01x slower                                                         |
| json_loads                      | 10.6 us                                                                  | 10.7 us: 1.01x slower                                                        |
| many_optionals                  | 254 us                                                                   | 258 us: 1.01x slower                                                         |
| tomli_loads                     | 796 ms                                                                   | 806 ms: 1.01x slower                                                         |
| async_tree_eager                | 38.5 ms                                                                  | 39.0 ms: 1.01x slower                                                        |
| bench_thread_pool               | 429 us                                                                   | 434 us: 1.01x slower                                                         |
| bpe_tokeniser                   | 1.85 sec                                                                 | 1.87 sec: 1.01x slower                                                       |
| pathlib                         | 10.8 ms                                                                  | 11.0 ms: 1.01x slower                                                        |
| deepcopy                        | 99.1 us                                                                  | 101 us: 1.02x slower                                                         |
| bench_mp_pool                   | 44.7 ms                                                                  | 45.5 ms: 1.02x slower                                                        |
| gc_traversal                    | 2.06 ms                                                                  | 2.10 ms: 1.02x slower                                                        |
| nqueens                         | 38.8 ms                                                                  | 39.6 ms: 1.02x slower                                                        |
| xml_etree_process               | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                        |
| json                            | 1.85 ms                                                                  | 1.89 ms: 1.02x slower                                                        |
| pprint_safe_repr                | 259 ms                                                                   | 265 ms: 1.02x slower                                                         |
| create_gc_cycles                | 919 us                                                                   | 942 us: 1.03x slower                                                         |
| python_startup_no_site          | 6.35 ms                                                                  | 6.51 ms: 1.03x slower                                                        |
| 2to3                            | 110 ms                                                                   | 113 ms: 1.03x slower                                                         |
| scimark_sparse_mat_mult         | 1.92 ms                                                                  | 1.97 ms: 1.03x slower                                                        |
| logging_silent                  | 33.2 ns                                                                  | 34.1 ns: 1.03x slower                                                        |
| html5lib                        | 20.1 ms                                                                  | 20.6 ms: 1.03x slower                                                        |
| pprint_pformat                  | 529 ms                                                                   | 543 ms: 1.03x slower                                                         |
| python_startup                  | 8.81 ms                                                                  | 9.06 ms: 1.03x slower                                                        |
| pidigits                        | 162 ms                                                                   | 167 ms: 1.03x slower                                                         |
| docutils                        | 1.01 sec                                                                 | 1.05 sec: 1.03x slower                                                       |
| sphinx                          | 391 ms                                                                   | 404 ms: 1.03x slower                                                         |
| meteor_contest                  | 44.9 ms                                                                  | 46.5 ms: 1.04x slower                                                        |
| richards                        | 9.75 ms                                                                  | 10.1 ms: 1.04x slower                                                        |
| richards_super                  | 11.5 ms                                                                  | 11.9 ms: 1.04x slower                                                        |
| genshi_text                     | 8.99 ms                                                                  | 9.36 ms: 1.04x slower                                                        |
| sympy_expand                    | 176 ms                                                                   | 184 ms: 1.05x slower                                                         |
| scimark_monte_carlo             | 22.7 ms                                                                  | 23.8 ms: 1.05x slower                                                        |
| generators                      | 18.9 ms                                                                  | 19.9 ms: 1.05x slower                                                        |
| pycparser                       | 444 ms                                                                   | 470 ms: 1.06x slower                                                         |
| pyflate                         | 143 ms                                                                   | 152 ms: 1.06x slower                                                         |
| xml_etree_generate              | 31.4 ms                                                                  | 33.3 ms: 1.06x slower                                                        |
| genshi_xml                      | 21.1 ms                                                                  | 22.5 ms: 1.06x slower                                                        |
| sqlglot_v2_normalize            | 48.6 ms                                                                  | 52.4 ms: 1.08x slower                                                        |
| mdp                             | 578 ms                                                                   | 642 ms: 1.11x slower                                                         |
| sqlglot_v2_optimize             | 24.6 ms                                                                  | 27.7 ms: 1.12x slower                                                        |
| sympy_integrate                 | 7.63 ms                                                                  | 8.58 ms: 1.12x slower                                                        |
| pylint                          | 123 ms                                                                   | 140 ms: 1.14x slower                                                         |
| go                              | 42.7 ms                                                                  | 48.9 ms: 1.14x slower                                                        |
| sympy_str                       | 106 ms                                                                   | 122 ms: 1.14x slower                                                         |
| hexiom                          | 2.61 ms                                                                  | 3.01 ms: 1.15x slower                                                        |
| regex_compile                   | 40.4 ms                                                                  | 46.6 ms: 1.16x slower                                                        |
| sympy_sum                       | 56.8 ms                                                                  | 65.6 ms: 1.16x slower                                                        |
| comprehensions                  | 6.18 us                                                                  | 7.72 us: 1.25x slower                                                        |
| Geometric mean                  | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (10): regex_effbot, regex_dna, nbody, sqlite_synth, float, fannkuch, sqlglot_v2_transpile, spectral_norm, json_dumps, async_tree_eager_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 99.82% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x