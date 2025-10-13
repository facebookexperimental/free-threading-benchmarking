# Results vs. base

- fork: Fidget-Spinner
- ref: msvc_tailcall_take_t
- machine: linux-x86_64
- commit hash: 0786133
- commit date: 2025-10-11
- overall geometric mean: 1.001x slower
- HPT reliability: 77.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 279 ms                                                                | 281 ms: 1.01x slower                                                            |
| docutils       | 2.70 sec                                                              | 2.72 sec: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                                    |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 486 ms                                                                | 473 ms: 1.03x faster                                                            |
| async_tree_cpu_io_mixed    | 513 ms                                                                | 499 ms: 1.03x faster                                                            |
| async_generators           | 359 ms                                                                | 366 ms: 1.02x slower                                                            |
| coroutines                 | 24.1 ms                                                               | 24.6 ms: 1.02x slower                                                           |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                                    |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_memoization_tg, async_tree_io, asyncio_websockets, async_tree_memoization, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 215 ms                                                                | 204 ms: 1.06x faster                                                            |
| nbody          | 126 ms                                                                | 126 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                | 143 ms: 1.00x faster                                                            |
| regex_v8       | 20.1 ms                                                               | 21.0 ms: 1.04x slower                                                           |
| regex_dna      | 166 ms                                                                | 174 ms: 1.05x slower                                                            |
| regex_effbot   | 2.58 ms                                                               | 2.71 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 343 us                                                                | 340 us: 1.01x faster                                                            |
| xml_etree_parse      | 130 ms                                                                | 130 ms: 1.00x faster                                                            |
| xml_etree_process    | 69.4 ms                                                               | 69.7 ms: 1.00x slower                                                           |
| unpickle_pure_python | 236 us                                                                | 237 us: 1.01x slower                                                            |
| xml_etree_iterparse  | 86.7 ms                                                               | 88.3 ms: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                                    |

Benchmark hidden because not significant (4): xml_etree_generate, tomli_loads, json_dumps, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                               | 15.7 ms: 1.00x slower                                                           |
| python_startup_no_site | 9.56 ms                                                               | 9.57 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 27.1 ms                                                               | 26.8 ms: 1.01x faster                                                           |
| genshi_xml      | 58.5 ms                                                               | 57.8 ms: 1.01x faster                                                           |
| django_template | 41.3 ms                                                               | 41.8 ms: 1.01x slower                                                           |
| mako            | 15.4 ms                                                               | 16.0 ms: 1.04x slower                                                           |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits                   | 215 ms                                                                | 204 ms: 1.06x faster                                                            |
| logging_silent             | 109 ns                                                                | 105 ns: 1.04x faster                                                            |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                | 473 ms: 1.03x faster                                                            |
| async_tree_cpu_io_mixed    | 513 ms                                                                | 499 ms: 1.03x faster                                                            |
| pyflate                    | 466 ms                                                                | 454 ms: 1.03x faster                                                            |
| pycparser                  | 1.17 sec                                                              | 1.14 sec: 1.03x faster                                                          |
| richards                   | 52.1 ms                                                               | 50.9 ms: 1.02x faster                                                           |
| hexiom                     | 6.49 ms                                                               | 6.36 ms: 1.02x faster                                                           |
| raytrace                   | 306 ms                                                                | 300 ms: 1.02x faster                                                            |
| richards_super             | 60.1 ms                                                               | 59.1 ms: 1.02x faster                                                           |
| go                         | 124 ms                                                                | 122 ms: 1.02x faster                                                            |
| deltablue                  | 3.59 ms                                                               | 3.53 ms: 1.02x faster                                                           |
| genshi_text                | 27.1 ms                                                               | 26.8 ms: 1.01x faster                                                           |
| crypto_pyaes               | 86.5 ms                                                               | 85.4 ms: 1.01x faster                                                           |
| genshi_xml                 | 58.5 ms                                                               | 57.8 ms: 1.01x faster                                                           |
| dulwich_log                | 73.0 ms                                                               | 72.3 ms: 1.01x faster                                                           |
| telco                      | 177 ms                                                                | 176 ms: 1.01x faster                                                            |
| pickle_pure_python         | 343 us                                                                | 340 us: 1.01x faster                                                            |
| sympy_sum                  | 178 ms                                                                | 177 ms: 1.01x faster                                                            |
| chaos                      | 63.9 ms                                                               | 63.5 ms: 1.01x faster                                                           |
| deepcopy_reduce            | 2.96 us                                                               | 2.94 us: 1.00x faster                                                           |
| regex_compile              | 143 ms                                                                | 143 ms: 1.00x faster                                                            |
| bpe_tokeniser              | 4.40 sec                                                              | 4.39 sec: 1.00x faster                                                          |
| comprehensions             | 17.8 us                                                               | 17.8 us: 1.00x faster                                                           |
| xml_etree_parse            | 130 ms                                                                | 130 ms: 1.00x faster                                                            |
| python_startup             | 15.7 ms                                                               | 15.7 ms: 1.00x slower                                                           |
| bench_thread_pool          | 3.06 ms                                                               | 3.06 ms: 1.00x slower                                                           |
| python_startup_no_site     | 9.56 ms                                                               | 9.57 ms: 1.00x slower                                                           |
| sympy_integrate            | 21.9 ms                                                               | 22.0 ms: 1.00x slower                                                           |
| sympy_str                  | 309 ms                                                                | 311 ms: 1.00x slower                                                            |
| xml_etree_process          | 69.4 ms                                                               | 69.7 ms: 1.00x slower                                                           |
| nbody                      | 126 ms                                                                | 126 ms: 1.00x slower                                                            |
| sympy_expand               | 517 ms                                                                | 519 ms: 1.00x slower                                                            |
| unpickle_pure_python       | 236 us                                                                | 237 us: 1.01x slower                                                            |
| 2to3                       | 279 ms                                                                | 281 ms: 1.01x slower                                                            |
| scimark_fft                | 342 ms                                                                | 344 ms: 1.01x slower                                                            |
| spectral_norm              | 109 ms                                                                | 110 ms: 1.01x slower                                                            |
| pathlib                    | 18.0 ms                                                               | 18.1 ms: 1.01x slower                                                           |
| typing_runtime_protocols   | 186 us                                                                | 187 us: 1.01x slower                                                            |
| docutils                   | 2.70 sec                                                              | 2.72 sec: 1.01x slower                                                          |
| gc_traversal               | 1.92 ms                                                               | 1.94 ms: 1.01x slower                                                           |
| create_gc_cycles           | 1.49 ms                                                               | 1.51 ms: 1.01x slower                                                           |
| pprint_pformat             | 1.62 sec                                                              | 1.63 sec: 1.01x slower                                                          |
| pprint_safe_repr           | 782 ms                                                                | 790 ms: 1.01x slower                                                            |
| django_template            | 41.3 ms                                                               | 41.8 ms: 1.01x slower                                                           |
| generators                 | 30.7 ms                                                               | 31.1 ms: 1.01x slower                                                           |
| thrift                     | 872 us                                                                | 884 us: 1.01x slower                                                            |
| scimark_lu                 | 130 ms                                                                | 132 ms: 1.02x slower                                                            |
| xml_etree_iterparse        | 86.7 ms                                                               | 88.3 ms: 1.02x slower                                                           |
| async_generators           | 359 ms                                                                | 366 ms: 1.02x slower                                                            |
| meteor_contest             | 118 ms                                                                | 121 ms: 1.02x slower                                                            |
| coroutines                 | 24.1 ms                                                               | 24.6 ms: 1.02x slower                                                           |
| scimark_sparse_mat_mult    | 5.13 ms                                                               | 5.32 ms: 1.04x slower                                                           |
| mako                       | 15.4 ms                                                               | 16.0 ms: 1.04x slower                                                           |
| regex_v8                   | 20.1 ms                                                               | 21.0 ms: 1.04x slower                                                           |
| regex_dna                  | 166 ms                                                                | 174 ms: 1.05x slower                                                            |
| regex_effbot               | 2.58 ms                                                               | 2.71 ms: 1.05x slower                                                           |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                                    |

Benchmark hidden because not significant (37): subparsers, sqlite_synth, async_tree_io_tg, async_tree_memoization_tg, async_tree_io, sqlglot_v2_parse, deepcopy_memo, bench_mp_pool, coverage, connected_components, many_optionals, k_core, shortest_path, xml_etree_generate, sqlglot_v2_normalize, float, sqlglot_v2_optimize, asyncio_websockets, pylint, mdp, logging_simple, nqueens, tomli_loads, html5lib, deepcopy, fannkuch, async_tree_memoization, json_dumps, scimark_monte_carlo, sphinx, sqlglot_v2_transpile, async_tree_none_tg, json_loads, json, scimark_sor, async_tree_none, logging_format

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 77.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x