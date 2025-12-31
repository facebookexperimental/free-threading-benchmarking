# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 2e5e9e6
- commit date: 2025-12-31
- overall geometric mean: 1.010x slower
- HPT reliability: 96.39%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 111 ms: 1.01x slower                                                         |
| docutils       | 1.01 sec                                                                 | 1.05 sec: 1.04x slower                                                       |
| sphinx         | 391 ms                                                                   | 411 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 224 ms                                                                   | 214 ms: 1.05x faster                                                         |
| async_tree_none_tg         | 98.2 ms                                                                  | 94.9 ms: 1.04x faster                                                        |
| async_tree_eager_io_tg     | 222 ms                                                                   | 215 ms: 1.03x faster                                                         |
| async_tree_memoization_tg  | 136 ms                                                                   | 132 ms: 1.03x faster                                                         |
| async_tree_io              | 231 ms                                                                   | 227 ms: 1.02x faster                                                         |
| async_tree_none            | 98.9 ms                                                                  | 97.2 ms: 1.02x faster                                                        |
| async_tree_eager_tg        | 80.7 ms                                                                  | 79.3 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed_tg | 254 ms                                                                   | 251 ms: 1.01x faster                                                         |
| async_generators           | 184 ms                                                                   | 183 ms: 1.01x faster                                                         |
| asyncio_websockets         | 188 ms                                                                   | 188 ms: 1.00x slower                                                         |
| async_tree_eager           | 38.5 ms                                                                  | 38.8 ms: 1.01x slower                                                        |
| coroutines                 | 10.2 ms                                                                  | 10.4 ms: 1.01x slower                                                        |
| Geometric mean             | (ref)                                                                    | 1.01x faster                                                                 |

Benchmark hidden because not significant (7): async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 24.4 ms                                                                  | 24.1 ms: 1.01x faster                                                        |
| pidigits       | 162 ms                                                                   | 165 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.46 ms                                                                  | 1.47 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|---------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse     | 63.9 ms                                                                  | 61.6 ms: 1.04x faster                                                        |
| xml_etree_iterparse | 38.6 ms                                                                  | 37.7 ms: 1.02x faster                                                        |
| json_dumps          | 3.68 ms                                                                  | 3.64 ms: 1.01x faster                                                        |
| pickle_pure_python  | 112 us                                                                   | 114 us: 1.01x slower                                                         |
| xml_etree_process   | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                        |
| xml_etree_generate  | 31.4 ms                                                                  | 32.6 ms: 1.04x slower                                                        |
| Geometric mean      | (ref)                                                                    | 1.00x slower                                                                 |

Benchmark hidden because not significant (3): json_loads, unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.35 ms                                                                  | 6.45 ms: 1.02x slower                                                        |
| python_startup         | 8.81 ms                                                                  | 8.95 ms: 1.02x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.9 ms                                                                  | 13.1 ms: 1.06x faster                                                        |
| mako            | 4.14 ms                                                                  | 4.12 ms: 1.00x faster                                                        |
| genshi_text     | 8.99 ms                                                                  | 9.58 ms: 1.07x slower                                                        |
| genshi_xml      | 21.1 ms                                                                  | 22.8 ms: 1.08x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_format             | 2.34 us                                                                  | 1.98 us: 1.18x faster                                                        |
| logging_simple             | 2.14 us                                                                  | 1.81 us: 1.18x faster                                                        |
| scimark_sor                | 42.3 ms                                                                  | 38.2 ms: 1.11x faster                                                        |
| django_template            | 13.9 ms                                                                  | 13.1 ms: 1.06x faster                                                        |
| scimark_lu                 | 36.7 ms                                                                  | 34.6 ms: 1.06x faster                                                        |
| coverage                   | 33.8 ms                                                                  | 32.1 ms: 1.05x faster                                                        |
| async_tree_io_tg           | 224 ms                                                                   | 214 ms: 1.05x faster                                                         |
| xml_etree_parse            | 63.9 ms                                                                  | 61.6 ms: 1.04x faster                                                        |
| chaos                      | 22.1 ms                                                                  | 21.3 ms: 1.04x faster                                                        |
| async_tree_none_tg         | 98.2 ms                                                                  | 94.9 ms: 1.04x faster                                                        |
| async_tree_eager_io_tg     | 222 ms                                                                   | 215 ms: 1.03x faster                                                         |
| async_tree_memoization_tg  | 136 ms                                                                   | 132 ms: 1.03x faster                                                         |
| xml_etree_iterparse        | 38.6 ms                                                                  | 37.7 ms: 1.02x faster                                                        |
| async_tree_io              | 231 ms                                                                   | 227 ms: 1.02x faster                                                         |
| async_tree_none            | 98.9 ms                                                                  | 97.2 ms: 1.02x faster                                                        |
| raytrace                   | 106 ms                                                                   | 104 ms: 1.02x faster                                                         |
| async_tree_eager_tg        | 80.7 ms                                                                  | 79.3 ms: 1.02x faster                                                        |
| deepcopy_reduce            | 1.03 us                                                                  | 1.01 us: 1.02x faster                                                        |
| telco                      | 2.61 ms                                                                  | 2.57 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed_tg | 254 ms                                                                   | 251 ms: 1.01x faster                                                         |
| float                      | 24.4 ms                                                                  | 24.1 ms: 1.01x faster                                                        |
| json_dumps                 | 3.68 ms                                                                  | 3.64 ms: 1.01x faster                                                        |
| sqlite_synth               | 974 ns                                                                   | 964 ns: 1.01x faster                                                         |
| fannkuch                   | 154 ms                                                                   | 153 ms: 1.01x faster                                                         |
| subparsers                 | 3.92 ms                                                                  | 3.90 ms: 1.01x faster                                                        |
| async_generators           | 184 ms                                                                   | 183 ms: 1.01x faster                                                         |
| mako                       | 4.14 ms                                                                  | 4.12 ms: 1.00x faster                                                        |
| generators                 | 18.9 ms                                                                  | 18.8 ms: 1.00x faster                                                        |
| scimark_fft                | 102 ms                                                                   | 101 ms: 1.00x faster                                                         |
| asyncio_websockets         | 188 ms                                                                   | 188 ms: 1.00x slower                                                         |
| scimark_sparse_mat_mult    | 1.92 ms                                                                  | 1.93 ms: 1.01x slower                                                        |
| gc_traversal               | 2.06 ms                                                                  | 2.07 ms: 1.01x slower                                                        |
| nqueens                    | 38.8 ms                                                                  | 39.1 ms: 1.01x slower                                                        |
| deepcopy_memo              | 11.8 us                                                                  | 11.9 us: 1.01x slower                                                        |
| shortest_path              | 215 ms                                                                   | 217 ms: 1.01x slower                                                         |
| 2to3                       | 110 ms                                                                   | 111 ms: 1.01x slower                                                         |
| bench_mp_pool              | 44.7 ms                                                                  | 45.0 ms: 1.01x slower                                                        |
| async_tree_eager           | 38.5 ms                                                                  | 38.8 ms: 1.01x slower                                                        |
| create_gc_cycles           | 919 us                                                                   | 927 us: 1.01x slower                                                         |
| typing_runtime_protocols   | 62.9 us                                                                  | 63.5 us: 1.01x slower                                                        |
| pathlib                    | 10.8 ms                                                                  | 10.9 ms: 1.01x slower                                                        |
| bpe_tokeniser              | 1.85 sec                                                                 | 1.87 sec: 1.01x slower                                                       |
| pickle_pure_python         | 112 us                                                                   | 114 us: 1.01x slower                                                         |
| scimark_monte_carlo        | 22.7 ms                                                                  | 23.0 ms: 1.01x slower                                                        |
| many_optionals             | 254 us                                                                   | 258 us: 1.01x slower                                                         |
| regex_effbot               | 1.46 ms                                                                  | 1.47 ms: 1.01x slower                                                        |
| bench_thread_pool          | 429 us                                                                   | 434 us: 1.01x slower                                                         |
| coroutines                 | 10.2 ms                                                                  | 10.4 ms: 1.01x slower                                                        |
| thrift                     | 290 us                                                                   | 294 us: 1.01x slower                                                         |
| deepcopy                   | 99.1 us                                                                  | 101 us: 1.01x slower                                                         |
| python_startup_no_site     | 6.35 ms                                                                  | 6.45 ms: 1.02x slower                                                        |
| python_startup             | 8.81 ms                                                                  | 8.95 ms: 1.02x slower                                                        |
| pidigits                   | 162 ms                                                                   | 165 ms: 1.02x slower                                                         |
| sqlglot_v2_parse           | 471 us                                                                   | 481 us: 1.02x slower                                                         |
| xml_etree_process          | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                        |
| meteor_contest             | 44.9 ms                                                                  | 45.9 ms: 1.02x slower                                                        |
| logging_silent             | 33.2 ns                                                                  | 34.0 ns: 1.02x slower                                                        |
| docutils                   | 1.01 sec                                                                 | 1.05 sec: 1.04x slower                                                       |
| sqlglot_v2_normalize       | 48.6 ms                                                                  | 50.3 ms: 1.04x slower                                                        |
| sqlglot_v2_transpile       | 598 us                                                                   | 620 us: 1.04x slower                                                         |
| hexiom                     | 2.61 ms                                                                  | 2.71 ms: 1.04x slower                                                        |
| xml_etree_generate         | 31.4 ms                                                                  | 32.6 ms: 1.04x slower                                                        |
| deltablue                  | 1.13 ms                                                                  | 1.17 ms: 1.04x slower                                                        |
| pycparser                  | 444 ms                                                                   | 462 ms: 1.04x slower                                                         |
| sympy_expand               | 176 ms                                                                   | 184 ms: 1.04x slower                                                         |
| sphinx                     | 391 ms                                                                   | 411 ms: 1.05x slower                                                         |
| pprint_pformat             | 529 ms                                                                   | 559 ms: 1.06x slower                                                         |
| genshi_text                | 8.99 ms                                                                  | 9.58 ms: 1.07x slower                                                        |
| pprint_safe_repr           | 259 ms                                                                   | 278 ms: 1.07x slower                                                         |
| genshi_xml                 | 21.1 ms                                                                  | 22.8 ms: 1.08x slower                                                        |
| sympy_str                  | 106 ms                                                                   | 115 ms: 1.08x slower                                                         |
| pyflate                    | 143 ms                                                                   | 155 ms: 1.08x slower                                                         |
| go                         | 42.7 ms                                                                  | 46.3 ms: 1.08x slower                                                        |
| sympy_sum                  | 56.8 ms                                                                  | 61.7 ms: 1.09x slower                                                        |
| mdp                        | 578 ms                                                                   | 632 ms: 1.09x slower                                                         |
| sqlglot_v2_optimize        | 24.6 ms                                                                  | 27.1 ms: 1.10x slower                                                        |
| sympy_integrate            | 7.63 ms                                                                  | 8.50 ms: 1.11x slower                                                        |
| pylint                     | 123 ms                                                                   | 141 ms: 1.15x slower                                                         |
| richards_super             | 11.5 ms                                                                  | 13.4 ms: 1.17x slower                                                        |
| richards                   | 9.75 ms                                                                  | 11.6 ms: 1.19x slower                                                        |
| Geometric mean             | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (22): async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_memoization, async_tree_cpu_io_mixed, regex_compile, regex_v8, spectral_norm, regex_dna, json_loads, crypto_pyaes, async_tree_eager_cpu_io_mixed, k_core, nbody, unpickle_pure_python, dulwich_log, comprehensions, connected_components, tomli_loads, async_tree_eager_cpu_io_mixed_tg, html5lib, json, async_tree_eager_memoization

- Geometric mean (including insignificant results): 1.010x slower

# HPT report

- Reliability score: 96.39% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x