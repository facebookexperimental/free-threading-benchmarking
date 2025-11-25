# Results vs. base

- fork: Fidget-Spinner
- ref: jit_lower_trace_limi
- machine: darwin-arm64
- commit hash: f96af45
- commit date: 2025-11-24
- overall geometric mean: 1.002x slower
- HPT reliability: 95.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| 2to3           | 118 ms                                                   | 116 ms: 1.01x faster                                                               |
| html5lib       | 23.4 ms                                                  | 23.1 ms: 1.01x faster                                                              |
| sphinx         | 8.74 ms                                                  | 8.71 ms: 1.00x faster                                                              |
| Geometric mean | (ref)                                                    | 1.01x faster                                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| coroutines                    | 10.1 ms                                                  | 9.92 ms: 1.02x faster                                                              |
| async_generators              | 188 ms                                                   | 185 ms: 1.02x faster                                                               |
| async_tree_eager_io           | 228 ms                                                   | 224 ms: 1.02x faster                                                               |
| async_tree_eager              | 42.9 ms                                                  | 42.3 ms: 1.01x faster                                                              |
| async_tree_eager_tg           | 83.0 ms                                                  | 82.0 ms: 1.01x faster                                                              |
| async_tree_eager_cpu_io_mixed | 226 ms                                                   | 225 ms: 1.00x faster                                                               |
| Geometric mean                | (ref)                                                    | 1.01x faster                                                                       |

Benchmark hidden because not significant (13): async_tree_none, async_tree_eager_memoization, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_io_tg, async_tree_eager_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| pidigits       | 167 ms                                                   | 167 ms: 1.00x faster                                                               |
| nbody          | 54.1 ms                                                  | 55.4 ms: 1.02x slower                                                              |
| Geometric mean | (ref)                                                    | 1.01x slower                                                                       |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| regex_v8       | 9.72 ms                                                  | 9.61 ms: 1.01x faster                                                              |
| regex_compile  | 45.5 ms                                                  | 45.2 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                    | 1.01x faster                                                                       |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| pickle_pure_python   | 132 us                                                   | 133 us: 1.01x slower                                                               |
| unpickle_pure_python | 93.9 us                                                  | 95.0 us: 1.01x slower                                                              |
| xml_etree_iterparse  | 38.3 ms                                                  | 39.7 ms: 1.04x slower                                                              |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                                       |

Benchmark hidden because not significant (6): xml_etree_parse, json_loads, xml_etree_generate, xml_etree_process, json_dumps, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| python_startup | 9.10 ms                                                  | 9.09 ms: 1.00x faster                                                              |
| Geometric mean | (ref)                                                    | 1.00x faster                                                                       |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| django_template | 14.8 ms                                                  | 14.7 ms: 1.01x faster                                                              |
| mako            | 4.37 ms                                                  | 4.40 ms: 1.01x slower                                                              |
| genshi_text     | 10.3 ms                                                  | 10.5 ms: 1.02x slower                                                              |
| genshi_xml      | 23.6 ms                                                  | 24.0 ms: 1.02x slower                                                              |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                                       |

All benchmarks:
===============

| Benchmark                     | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| many_optionals                | 384 us                                                   | 374 us: 1.03x faster                                                               |
| sympy_integrate               | 8.65 ms                                                  | 8.43 ms: 1.03x faster                                                              |
| sympy_sum                     | 62.3 ms                                                  | 60.8 ms: 1.03x faster                                                              |
| go                            | 59.5 ms                                                  | 58.2 ms: 1.02x faster                                                              |
| coroutines                    | 10.1 ms                                                  | 9.92 ms: 1.02x faster                                                              |
| logging_simple                | 2.26 us                                                  | 2.21 us: 1.02x faster                                                              |
| logging_format                | 2.48 us                                                  | 2.44 us: 1.02x faster                                                              |
| create_gc_cycles              | 949 us                                                   | 933 us: 1.02x faster                                                               |
| async_generators              | 188 ms                                                   | 185 ms: 1.02x faster                                                               |
| async_tree_eager_io           | 228 ms                                                   | 224 ms: 1.02x faster                                                               |
| deepcopy                      | 102 us                                                   | 100 us: 1.02x faster                                                               |
| async_tree_eager              | 42.9 ms                                                  | 42.3 ms: 1.01x faster                                                              |
| gc_traversal                  | 2.12 ms                                                  | 2.09 ms: 1.01x faster                                                              |
| html5lib                      | 23.4 ms                                                  | 23.1 ms: 1.01x faster                                                              |
| 2to3                          | 118 ms                                                   | 116 ms: 1.01x faster                                                               |
| scimark_sparse_mat_mult       | 2.02 ms                                                  | 2.00 ms: 1.01x faster                                                              |
| async_tree_eager_tg           | 83.0 ms                                                  | 82.0 ms: 1.01x faster                                                              |
| django_template               | 14.8 ms                                                  | 14.7 ms: 1.01x faster                                                              |
| regex_v8                      | 9.72 ms                                                  | 9.61 ms: 1.01x faster                                                              |
| subparsers                    | 18.5 ms                                                  | 18.3 ms: 1.01x faster                                                              |
| dulwich_log                   | 20.0 ms                                                  | 19.8 ms: 1.01x faster                                                              |
| sympy_expand                  | 185 ms                                                   | 183 ms: 1.01x faster                                                               |
| sqlglot_v2_normalize          | 49.8 ms                                                  | 49.3 ms: 1.01x faster                                                              |
| sqlglot_v2_transpile          | 666 us                                                   | 662 us: 1.01x faster                                                               |
| comprehensions                | 7.41 us                                                  | 7.36 us: 1.01x faster                                                              |
| bench_thread_pool             | 433 us                                                   | 430 us: 1.01x faster                                                               |
| regex_compile                 | 45.5 ms                                                  | 45.2 ms: 1.01x faster                                                              |
| deepcopy_reduce               | 1.04 us                                                  | 1.03 us: 1.01x faster                                                              |
| bench_mp_pool                 | 45.9 ms                                                  | 45.6 ms: 1.01x faster                                                              |
| async_tree_eager_cpu_io_mixed | 226 ms                                                   | 225 ms: 1.00x faster                                                               |
| sphinx                        | 8.74 ms                                                  | 8.71 ms: 1.00x faster                                                              |
| pidigits                      | 167 ms                                                   | 167 ms: 1.00x faster                                                               |
| python_startup                | 9.10 ms                                                  | 9.09 ms: 1.00x faster                                                              |
| spectral_norm                 | 48.6 ms                                                  | 48.7 ms: 1.00x slower                                                              |
| mako                          | 4.37 ms                                                  | 4.40 ms: 1.01x slower                                                              |
| deltablue                     | 1.54 ms                                                  | 1.55 ms: 1.01x slower                                                              |
| scimark_fft                   | 120 ms                                                   | 120 ms: 1.01x slower                                                               |
| pickle_pure_python            | 132 us                                                   | 133 us: 1.01x slower                                                               |
| pprint_pformat                | 591 ms                                                   | 595 ms: 1.01x slower                                                               |
| chaos                         | 27.4 ms                                                  | 27.6 ms: 1.01x slower                                                              |
| telco                         | 2.72 ms                                                  | 2.74 ms: 1.01x slower                                                              |
| unpickle_pure_python          | 93.9 us                                                  | 95.0 us: 1.01x slower                                                              |
| scimark_monte_carlo           | 27.8 ms                                                  | 28.1 ms: 1.01x slower                                                              |
| genshi_text                   | 10.3 ms                                                  | 10.5 ms: 1.02x slower                                                              |
| pprint_safe_repr              | 289 ms                                                   | 294 ms: 1.02x slower                                                               |
| scimark_lu                    | 50.5 ms                                                  | 51.5 ms: 1.02x slower                                                              |
| thrift                        | 299 us                                                   | 305 us: 1.02x slower                                                               |
| genshi_xml                    | 23.6 ms                                                  | 24.0 ms: 1.02x slower                                                              |
| nbody                         | 54.1 ms                                                  | 55.4 ms: 1.02x slower                                                              |
| fannkuch                      | 176 ms                                                   | 181 ms: 1.03x slower                                                               |
| xml_etree_iterparse           | 38.3 ms                                                  | 39.7 ms: 1.04x slower                                                              |
| richards_super                | 16.6 ms                                                  | 17.3 ms: 1.04x slower                                                              |
| logging_silent                | 48.6 ns                                                  | 51.4 ns: 1.06x slower                                                              |
| richards                      | 14.6 ms                                                  | 15.5 ms: 1.06x slower                                                              |
| raytrace                      | 121 ms                                                   | 132 ms: 1.09x slower                                                               |
| scimark_sor                   | 50.7 ms                                                  | 56.3 ms: 1.11x slower                                                              |
| Geometric mean                | (ref)                                                    | 1.00x slower                                                                       |

Benchmark hidden because not significant (42): async_tree_none, async_tree_eager_memoization, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_none_tg, async_tree_memoization, pylint, pycparser, async_tree_cpu_io_mixed, float, async_tree_io, xml_etree_parse, regex_effbot, mdp, sqlite_synth, async_tree_memoization_tg, sqlglot_v2_parse, regex_dna, sqlglot_v2_optimize, hexiom, async_tree_cpu_io_mixed_tg, asyncio_websockets, python_startup_no_site, json_loads, meteor_contest, xml_etree_generate, sympy_str, xml_etree_process, generators, json_dumps, crypto_pyaes, bpe_tokeniser, deepcopy_memo, pathlib, async_tree_io_tg, typing_runtime_protocols, nqueens, coverage, pyflate, async_tree_eager_io_tg, json, tomli_loads
Ignored benchmarks (1) of results/bm-20251124-3.15.0a2+-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45.json: dask

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 95.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x