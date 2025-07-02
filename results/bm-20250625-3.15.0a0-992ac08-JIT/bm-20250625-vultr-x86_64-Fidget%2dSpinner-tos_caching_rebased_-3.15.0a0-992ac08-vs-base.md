# Results vs. base

- fork: Fidget-Spinner
- ref: tos_caching_rebased_
- machine: linux-x86_64
- commit hash: 992ac08
- commit date: 2025-06-25
- overall geometric mean: 1.003x faster
- HPT reliability: 98.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization     | 312 ms                                                                | 308 ms: 1.01x faster                                                            |
| async_tree_memoization_tg  | 310 ms                                                                | 306 ms: 1.01x faster                                                            |
| async_tree_none_tg         | 255 ms                                                                | 253 ms: 1.01x faster                                                            |
| coroutines                 | 23.0 ms                                                               | 23.2 ms: 1.01x slower                                                           |
| async_tree_cpu_io_mixed_tg | 506 ms                                                                | 511 ms: 1.01x slower                                                            |
| async_tree_cpu_io_mixed    | 505 ms                                                                | 511 ms: 1.01x slower                                                            |
| async_generators           | 352 ms                                                                | 356 ms: 1.01x slower                                                            |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                                    |

Benchmark hidden because not significant (4): async_tree_io, async_tree_none, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 90.0 ms                                                               | 74.2 ms: 1.21x faster                                                           |
| pidigits       | 203 ms                                                                | 196 ms: 1.04x faster                                                            |
| float          | 65.2 ms                                                               | 64.1 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                                 | 1.09x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_v8       | 23.0 ms                                                               | 22.7 ms: 1.01x faster                                                           |
| regex_effbot   | 2.89 ms                                                               | 2.86 ms: 1.01x faster                                                           |
| regex_compile  | 125 ms                                                                | 124 ms: 1.01x faster                                                            |
| regex_dna      | 178 ms                                                                | 180 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 315 us                                                                | 309 us: 1.02x faster                                                            |
| json_dumps           | 10.7 ms                                                               | 10.6 ms: 1.01x faster                                                           |
| xml_etree_parse      | 130 ms                                                                | 129 ms: 1.01x faster                                                            |
| xml_etree_process    | 55.2 ms                                                               | 54.6 ms: 1.01x faster                                                           |
| xml_etree_generate   | 79.1 ms                                                               | 78.1 ms: 1.01x faster                                                           |
| xml_etree_iterparse  | 91.8 ms                                                               | 92.3 ms: 1.01x slower                                                           |
| unpickle_pure_python | 191 us                                                                | 195 us: 1.02x slower                                                            |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                                    |

Benchmark hidden because not significant (2): json_loads, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.33 ms                                                               | 7.34 ms: 1.00x slower                                                           |
| python_startup         | 12.6 ms                                                               | 12.6 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| django_template | 34.3 ms                                                               | 34.6 ms: 1.01x slower                                                           |
| mako            | 11.2 ms                                                               | 11.4 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                                    |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody                      | 90.0 ms                                                               | 74.2 ms: 1.21x faster                                                           |
| fannkuch                   | 371 ms                                                                | 355 ms: 1.05x faster                                                            |
| spectral_norm              | 88.9 ms                                                               | 85.7 ms: 1.04x faster                                                           |
| pidigits                   | 203 ms                                                                | 196 ms: 1.04x faster                                                            |
| richards_super             | 36.0 ms                                                               | 35.0 ms: 1.03x faster                                                           |
| richards                   | 31.5 ms                                                               | 30.8 ms: 1.03x faster                                                           |
| logging_format             | 7.44 us                                                               | 7.26 us: 1.02x faster                                                           |
| thrift                     | 754 us                                                                | 737 us: 1.02x faster                                                            |
| scimark_fft                | 285 ms                                                                | 280 ms: 1.02x faster                                                            |
| bpe_tokeniser              | 4.04 sec                                                              | 3.97 sec: 1.02x faster                                                          |
| float                      | 65.2 ms                                                               | 64.1 ms: 1.02x faster                                                           |
| logging_simple             | 6.65 us                                                               | 6.53 us: 1.02x faster                                                           |
| pickle_pure_python         | 315 us                                                                | 309 us: 1.02x faster                                                            |
| nqueens                    | 76.5 ms                                                               | 75.4 ms: 1.02x faster                                                           |
| async_tree_memoization     | 312 ms                                                                | 308 ms: 1.01x faster                                                            |
| regex_v8                   | 23.0 ms                                                               | 22.7 ms: 1.01x faster                                                           |
| json_dumps                 | 10.7 ms                                                               | 10.6 ms: 1.01x faster                                                           |
| pyflate                    | 389 ms                                                                | 384 ms: 1.01x faster                                                            |
| async_tree_memoization_tg  | 310 ms                                                                | 306 ms: 1.01x faster                                                            |
| coverage                   | 81.4 ms                                                               | 80.4 ms: 1.01x faster                                                           |
| xml_etree_parse            | 130 ms                                                                | 129 ms: 1.01x faster                                                            |
| regex_effbot               | 2.89 ms                                                               | 2.86 ms: 1.01x faster                                                           |
| meteor_contest             | 102 ms                                                                | 101 ms: 1.01x faster                                                            |
| xml_etree_process          | 55.2 ms                                                               | 54.6 ms: 1.01x faster                                                           |
| xml_etree_generate         | 79.1 ms                                                               | 78.1 ms: 1.01x faster                                                           |
| scimark_monte_carlo        | 60.4 ms                                                               | 59.8 ms: 1.01x faster                                                           |
| deepcopy                   | 254 us                                                                | 251 us: 1.01x faster                                                            |
| generators                 | 28.6 ms                                                               | 28.3 ms: 1.01x faster                                                           |
| pathlib                    | 19.4 ms                                                               | 19.2 ms: 1.01x faster                                                           |
| create_gc_cycles           | 1.93 ms                                                               | 1.91 ms: 1.01x faster                                                           |
| deepcopy_memo              | 28.6 us                                                               | 28.4 us: 1.01x faster                                                           |
| sqlglot_v2_transpile       | 1.55 ms                                                               | 1.54 ms: 1.01x faster                                                           |
| sqlglot_v2_normalize       | 100 ms                                                                | 99.6 ms: 1.01x faster                                                           |
| sqlglot_v2_parse           | 1.24 ms                                                               | 1.23 ms: 1.01x faster                                                           |
| async_tree_none_tg         | 255 ms                                                                | 253 ms: 1.01x faster                                                            |
| shortest_path              | 439 ms                                                                | 436 ms: 1.01x faster                                                            |
| regex_compile              | 125 ms                                                                | 124 ms: 1.01x faster                                                            |
| dulwich_log                | 67.7 ms                                                               | 67.3 ms: 1.01x faster                                                           |
| deepcopy_reduce            | 2.66 us                                                               | 2.64 us: 1.01x faster                                                           |
| deltablue                  | 2.86 ms                                                               | 2.85 ms: 1.01x faster                                                           |
| go                         | 117 ms                                                                | 117 ms: 1.01x faster                                                            |
| bench_thread_pool          | 1.05 ms                                                               | 1.05 ms: 1.00x faster                                                           |
| python_startup_no_site     | 7.33 ms                                                               | 7.34 ms: 1.00x slower                                                           |
| python_startup             | 12.6 ms                                                               | 12.6 ms: 1.00x slower                                                           |
| chaos                      | 56.4 ms                                                               | 56.6 ms: 1.00x slower                                                           |
| xml_etree_iterparse        | 91.8 ms                                                               | 92.3 ms: 1.01x slower                                                           |
| bench_mp_pool              | 98.5 ms                                                               | 99.1 ms: 1.01x slower                                                           |
| coroutines                 | 23.0 ms                                                               | 23.2 ms: 1.01x slower                                                           |
| django_template            | 34.3 ms                                                               | 34.6 ms: 1.01x slower                                                           |
| async_tree_cpu_io_mixed_tg | 506 ms                                                                | 511 ms: 1.01x slower                                                            |
| json                       | 5.03 ms                                                               | 5.08 ms: 1.01x slower                                                           |
| async_tree_cpu_io_mixed    | 505 ms                                                                | 511 ms: 1.01x slower                                                            |
| regex_dna                  | 178 ms                                                                | 180 ms: 1.01x slower                                                            |
| async_generators           | 352 ms                                                                | 356 ms: 1.01x slower                                                            |
| scimark_sor                | 107 ms                                                                | 108 ms: 1.01x slower                                                            |
| mako                       | 11.2 ms                                                               | 11.4 ms: 1.02x slower                                                           |
| unpickle_pure_python       | 191 us                                                                | 195 us: 1.02x slower                                                            |
| telco                      | 7.25 ms                                                               | 7.40 ms: 1.02x slower                                                           |
| hexiom                     | 6.06 ms                                                               | 6.19 ms: 1.02x slower                                                           |
| comprehensions             | 16.6 us                                                               | 17.0 us: 1.02x slower                                                           |
| pprint_pformat             | 1.70 sec                                                              | 1.78 sec: 1.05x slower                                                          |
| scimark_sparse_mat_mult    | 4.50 ms                                                               | 4.73 ms: 1.05x slower                                                           |
| pprint_safe_repr           | 815 ms                                                                | 857 ms: 1.05x slower                                                            |
| gc_traversal               | 4.39 ms                                                               | 4.87 ms: 1.11x slower                                                           |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                                    |

Benchmark hidden because not significant (30): async_tree_io, html5lib, pycparser, sqlite_synth, sphinx, scimark_lu, async_tree_none, json_loads, k_core, tomli_loads, docutils, 2to3, mdp, raytrace, many_optionals, asyncio_websockets, sympy_expand, async_tree_io_tg, sqlglot_v2_optimize, sympy_integrate, pylint, sympy_sum, genshi_text, logging_silent, sympy_str, typing_runtime_protocols, subparsers, genshi_xml, crypto_pyaes, connected_components

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 98.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x