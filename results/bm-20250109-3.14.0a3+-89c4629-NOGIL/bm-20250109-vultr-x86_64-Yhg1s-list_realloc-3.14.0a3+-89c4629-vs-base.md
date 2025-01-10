# Results vs. base

- fork: Yhg1s
- ref: list_realloc
- machine: linux-x86_64
- commit hash: 89c4629
- commit date: 2025-01-09
- overall geometric mean: 1.003x faster
- HPT reliability: 91.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 347 ms                                                                 | 346 ms: 1.00x faster                                          |
| html5lib       | 91.0 ms                                                                | 90.3 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io              | 763 ms                                                                 | 759 ms: 1.01x faster                                          |
| async_generators           | 444 ms                                                                 | 446 ms: 1.00x slower                                          |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                 | 566 ms: 1.01x slower                                          |
| coroutines                 | 22.8 ms                                                                | 23.2 ms: 1.02x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (7): async_tree_memoization_tg, async_tree_none, async_tree_memoization, asyncio_websockets, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 184 ms: 1.09x faster                                          |
| float          | 108 ms                                                                 | 106 ms: 1.01x faster                                          |
| nbody          | 131 ms                                                                 | 130 ms: 1.01x faster                                          |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 2.95 ms                                                                | 2.85 ms: 1.04x faster                                         |
| regex_v8       | 25.5 ms                                                                | 25.4 ms: 1.00x faster                                         |
| regex_compile  | 167 ms                                                                 | 167 ms: 1.00x slower                                          |
| regex_dna      | 182 ms                                                                 | 187 ms: 1.03x slower                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|---------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle_pure_python  | 499 us                                                                 | 486 us: 1.03x faster                                          |
| json_loads          | 29.1 us                                                                | 28.6 us: 1.02x faster                                         |
| xml_etree_iterparse | 90.8 ms                                                                | 89.3 ms: 1.02x faster                                         |
| xml_etree_parse     | 130 ms                                                                 | 129 ms: 1.01x faster                                          |
| tomli_loads         | 2.36 sec                                                               | 2.37 sec: 1.00x slower                                        |
| xml_etree_process   | 73.8 ms                                                                | 74.1 ms: 1.00x slower                                         |
| xml_etree_generate  | 97.8 ms                                                                | 98.3 ms: 1.00x slower                                         |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                  |

Benchmark hidden because not significant (2): unpickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                         |
| python_startup_no_site | 9.80 ms                                                                | 9.79 ms: 1.00x faster                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                         |
| django_template | 49.4 ms                                                                | 49.7 ms: 1.01x slower                                         |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250109-vultr-x86_64-python-b725297cee9e5608b709-3.14.0a3+-b725297 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits                   | 199 ms                                                                 | 184 ms: 1.09x faster                                          |
| richards                   | 68.0 ms                                                                | 65.1 ms: 1.04x faster                                         |
| regex_effbot               | 2.95 ms                                                                | 2.85 ms: 1.04x faster                                         |
| deltablue                  | 7.37 ms                                                                | 7.13 ms: 1.03x faster                                         |
| logging_silent             | 185 ns                                                                 | 179 ns: 1.03x faster                                          |
| spectral_norm              | 113 ms                                                                 | 110 ms: 1.03x faster                                          |
| pickle_pure_python         | 499 us                                                                 | 486 us: 1.03x faster                                          |
| json_loads                 | 29.1 us                                                                | 28.6 us: 1.02x faster                                         |
| mdp                        | 2.78 sec                                                               | 2.73 sec: 1.02x faster                                        |
| generators                 | 39.3 ms                                                                | 38.6 ms: 1.02x faster                                         |
| xml_etree_iterparse        | 90.8 ms                                                                | 89.3 ms: 1.02x faster                                         |
| go                         | 234 ms                                                                 | 231 ms: 1.01x faster                                          |
| float                      | 108 ms                                                                 | 106 ms: 1.01x faster                                          |
| thrift                     | 1.02 ms                                                                | 1.01 ms: 1.01x faster                                         |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                          |
| hexiom                     | 9.32 ms                                                                | 9.21 ms: 1.01x faster                                         |
| deepcopy_reduce            | 3.42 us                                                                | 3.38 us: 1.01x faster                                         |
| crypto_pyaes               | 90.5 ms                                                                | 89.4 ms: 1.01x faster                                         |
| bpe_tokeniser              | 4.98 sec                                                               | 4.93 sec: 1.01x faster                                        |
| mako                       | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                         |
| raytrace                   | 495 ms                                                                 | 491 ms: 1.01x faster                                          |
| comprehensions             | 27.6 us                                                                | 27.3 us: 1.01x faster                                         |
| nbody                      | 131 ms                                                                 | 130 ms: 1.01x faster                                          |
| shortest_path              | 549 ms                                                                 | 544 ms: 1.01x faster                                          |
| scimark_fft                | 381 ms                                                                 | 378 ms: 1.01x faster                                          |
| html5lib                   | 91.0 ms                                                                | 90.3 ms: 1.01x faster                                         |
| sqlglot_parse              | 2.32 ms                                                                | 2.30 ms: 1.01x faster                                         |
| async_tree_io              | 763 ms                                                                 | 759 ms: 1.01x faster                                          |
| sympy_sum                  | 194 ms                                                                 | 193 ms: 1.01x faster                                          |
| typing_runtime_protocols   | 207 us                                                                 | 205 us: 1.01x faster                                          |
| create_gc_cycles           | 1.83 ms                                                                | 1.82 ms: 1.01x faster                                         |
| regex_v8                   | 25.5 ms                                                                | 25.4 ms: 1.00x faster                                         |
| deepcopy_memo              | 40.8 us                                                                | 40.6 us: 1.00x faster                                         |
| 2to3                       | 347 ms                                                                 | 346 ms: 1.00x faster                                          |
| python_startup             | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                         |
| fannkuch                   | 485 ms                                                                 | 484 ms: 1.00x faster                                          |
| python_startup_no_site     | 9.80 ms                                                                | 9.79 ms: 1.00x faster                                         |
| regex_compile              | 167 ms                                                                 | 167 ms: 1.00x slower                                          |
| telco                      | 8.54 ms                                                                | 8.58 ms: 1.00x slower                                         |
| tomli_loads                | 2.36 sec                                                               | 2.37 sec: 1.00x slower                                        |
| async_generators           | 444 ms                                                                 | 446 ms: 1.00x slower                                          |
| xml_etree_process          | 73.8 ms                                                                | 74.1 ms: 1.00x slower                                         |
| xml_etree_generate         | 97.8 ms                                                                | 98.3 ms: 1.00x slower                                         |
| pprint_safe_repr           | 941 ms                                                                 | 946 ms: 1.01x slower                                          |
| sqlglot_normalize          | 132 ms                                                                 | 133 ms: 1.01x slower                                          |
| pyflate                    | 628 ms                                                                 | 632 ms: 1.01x slower                                          |
| bench_thread_pool          | 3.36 ms                                                                | 3.38 ms: 1.01x slower                                         |
| django_template            | 49.4 ms                                                                | 49.7 ms: 1.01x slower                                         |
| pprint_pformat             | 1.95 sec                                                               | 1.97 sec: 1.01x slower                                        |
| chaos                      | 94.3 ms                                                                | 95.3 ms: 1.01x slower                                         |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                 | 566 ms: 1.01x slower                                          |
| logging_simple             | 8.77 us                                                                | 8.90 us: 1.01x slower                                         |
| scimark_lu                 | 158 ms                                                                 | 160 ms: 1.01x slower                                          |
| coroutines                 | 22.8 ms                                                                | 23.2 ms: 1.02x slower                                         |
| logging_format             | 9.77 us                                                                | 9.96 us: 1.02x slower                                         |
| gc_traversal               | 3.21 ms                                                                | 3.29 ms: 1.02x slower                                         |
| regex_dna                  | 182 ms                                                                 | 187 ms: 1.03x slower                                          |
| richards_super             | 75.2 ms                                                                | 77.5 ms: 1.03x slower                                         |
| scimark_sparse_mat_mult    | 5.41 ms                                                                | 5.59 ms: 1.03x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (37): sqlglot_transpile, meteor_contest, async_tree_memoization_tg, json, pylint, async_tree_none, async_tree_memoization, pathlib, dulwich_log, unpickle_pure_python, pycparser, connected_components, sphinx, scimark_sor, genshi_text, nqueens, sqlite_synth, sympy_integrate, bench_mp_pool, genshi_xml, docutils, sympy_expand, asyncio_websockets, sympy_str, many_optionals, sqlalchemy_imperative, sqlglot_optimize, deepcopy, k_core, json_dumps, async_tree_io_tg, scimark_monte_carlo, sqlalchemy_declarative, subparsers, async_tree_cpu_io_mixed, coverage, async_tree_none_tg

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 91.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x