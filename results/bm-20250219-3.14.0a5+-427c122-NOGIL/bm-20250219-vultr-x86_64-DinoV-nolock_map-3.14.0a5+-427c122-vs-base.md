# Results vs. base

- fork: DinoV
- ref: nolock_map
- machine: linux-x86_64
- commit hash: 427c122
- commit date: 2025-02-19
- overall geometric mean: 1.001x faster
- HPT reliability: 97.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 303 ms                                                                 | 301 ms: 1.01x faster                                        |
| html5lib       | 70.0 ms                                                                | 70.8 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|--------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io      | 587 ms                                                                 | 582 ms: 1.01x faster                                        |
| coroutines         | 23.5 ms                                                                | 23.4 ms: 1.01x faster                                       |
| asyncio_websockets | 519 ms                                                                 | 517 ms: 1.00x faster                                        |
| async_generators   | 372 ms                                                                 | 373 ms: 1.00x slower                                        |
| Geometric mean     | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 76.8 ms                                                                | 75.7 ms: 1.01x faster                                       |
| nbody          | 130 ms                                                                 | 131 ms: 1.01x slower                                        |
| pidigits       | 191 ms                                                                 | 200 ms: 1.05x slower                                        |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 155 ms                                                                 | 154 ms: 1.01x faster                                        |
| regex_v8       | 23.1 ms                                                                | 23.3 ms: 1.01x slower                                       |
| regex_effbot   | 2.76 ms                                                                | 2.80 ms: 1.02x slower                                       |
| regex_dna      | 172 ms                                                                 | 185 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| tomli_loads         | 2.35 sec                                                               | 2.31 sec: 1.01x faster                                      |
| xml_etree_process   | 69.8 ms                                                                | 69.2 ms: 1.01x faster                                       |
| xml_etree_iterparse | 87.9 ms                                                                | 87.4 ms: 1.01x faster                                       |
| xml_etree_generate  | 95.3 ms                                                                | 95.6 ms: 1.00x slower                                       |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (5): json_dumps, pickle_pure_python, unpickle_pure_python, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 9.62 ms                                                                | 9.61 ms: 1.00x faster                                       |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| mako           | 15.7 ms                                                                | 15.8 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (3): django_template, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| logging_format           | 8.37 us                                                                | 8.06 us: 1.04x faster                                       |
| deepcopy_reduce          | 3.24 us                                                                | 3.12 us: 1.04x faster                                       |
| logging_simple           | 7.22 us                                                                | 7.02 us: 1.03x faster                                       |
| deltablue                | 3.87 ms                                                                | 3.79 ms: 1.02x faster                                       |
| generators               | 31.9 ms                                                                | 31.2 ms: 1.02x faster                                       |
| pyflate                  | 500 ms                                                                 | 491 ms: 1.02x faster                                        |
| thrift                   | 910 us                                                                 | 892 us: 1.02x faster                                        |
| spectral_norm            | 110 ms                                                                 | 108 ms: 1.02x faster                                        |
| float                    | 76.8 ms                                                                | 75.7 ms: 1.01x faster                                       |
| tomli_loads              | 2.35 sec                                                               | 2.31 sec: 1.01x faster                                      |
| typing_runtime_protocols | 200 us                                                                 | 197 us: 1.01x faster                                        |
| nqueens                  | 97.1 ms                                                                | 95.9 ms: 1.01x faster                                       |
| logging_silent           | 115 ns                                                                 | 114 ns: 1.01x faster                                        |
| sympy_expand             | 550 ms                                                                 | 544 ms: 1.01x faster                                        |
| sqlalchemy_declarative   | 157 ms                                                                 | 156 ms: 1.01x faster                                        |
| comprehensions           | 19.7 us                                                                | 19.5 us: 1.01x faster                                       |
| sqlglot_parse            | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                       |
| xml_etree_process        | 69.8 ms                                                                | 69.2 ms: 1.01x faster                                       |
| chaos                    | 70.5 ms                                                                | 69.9 ms: 1.01x faster                                       |
| raytrace                 | 325 ms                                                                 | 322 ms: 1.01x faster                                        |
| async_tree_io            | 587 ms                                                                 | 582 ms: 1.01x faster                                        |
| sqlglot_normalize        | 121 ms                                                                 | 120 ms: 1.01x faster                                        |
| coroutines               | 23.5 ms                                                                | 23.4 ms: 1.01x faster                                       |
| fannkuch                 | 491 ms                                                                 | 488 ms: 1.01x faster                                        |
| 2to3                     | 303 ms                                                                 | 301 ms: 1.01x faster                                        |
| scimark_monte_carlo      | 83.1 ms                                                                | 82.6 ms: 1.01x faster                                       |
| xml_etree_iterparse      | 87.9 ms                                                                | 87.4 ms: 1.01x faster                                       |
| regex_compile            | 155 ms                                                                 | 154 ms: 1.01x faster                                        |
| go                       | 140 ms                                                                 | 139 ms: 1.01x faster                                        |
| sympy_str                | 334 ms                                                                 | 333 ms: 1.01x faster                                        |
| richards                 | 55.4 ms                                                                | 55.2 ms: 1.00x faster                                       |
| deepcopy_memo            | 38.5 us                                                                | 38.4 us: 1.00x faster                                       |
| asyncio_websockets       | 519 ms                                                                 | 517 ms: 1.00x faster                                        |
| sympy_integrate          | 24.0 ms                                                                | 23.9 ms: 1.00x faster                                       |
| k_core                   | 2.31 sec                                                               | 2.30 sec: 1.00x faster                                      |
| hexiom                   | 7.35 ms                                                                | 7.32 ms: 1.00x faster                                       |
| python_startup_no_site   | 9.62 ms                                                                | 9.61 ms: 1.00x faster                                       |
| async_generators         | 372 ms                                                                 | 373 ms: 1.00x slower                                        |
| bpe_tokeniser            | 4.71 sec                                                               | 4.72 sec: 1.00x slower                                      |
| xml_etree_generate       | 95.3 ms                                                                | 95.6 ms: 1.00x slower                                       |
| gc_traversal             | 1.73 ms                                                                | 1.74 ms: 1.00x slower                                       |
| coverage                 | 97.4 ms                                                                | 97.9 ms: 1.00x slower                                       |
| mako                     | 15.7 ms                                                                | 15.8 ms: 1.01x slower                                       |
| mdp                      | 2.77 sec                                                               | 2.78 sec: 1.01x slower                                      |
| dulwich_log              | 82.5 ms                                                                | 83.1 ms: 1.01x slower                                       |
| bench_mp_pool            | 94.8 ms                                                                | 95.4 ms: 1.01x slower                                       |
| nbody                    | 130 ms                                                                 | 131 ms: 1.01x slower                                        |
| crypto_pyaes             | 87.2 ms                                                                | 87.9 ms: 1.01x slower                                       |
| scimark_lu               | 139 ms                                                                 | 140 ms: 1.01x slower                                        |
| regex_v8                 | 23.1 ms                                                                | 23.3 ms: 1.01x slower                                       |
| html5lib                 | 70.0 ms                                                                | 70.8 ms: 1.01x slower                                       |
| create_gc_cycles         | 1.37 ms                                                                | 1.38 ms: 1.01x slower                                       |
| regex_effbot             | 2.76 ms                                                                | 2.80 ms: 1.02x slower                                       |
| telco                    | 8.63 ms                                                                | 8.79 ms: 1.02x slower                                       |
| richards_super           | 64.8 ms                                                                | 66.3 ms: 1.02x slower                                       |
| pidigits                 | 191 ms                                                                 | 200 ms: 1.05x slower                                        |
| regex_dna                | 172 ms                                                                 | 185 ms: 1.07x slower                                        |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (39): sqlglot_transpile, sqlglot_optimize, django_template, json, sympy_sum, deepcopy, pprint_safe_repr, scimark_sor, genshi_xml, async_tree_cpu_io_mixed, json_dumps, async_tree_cpu_io_mixed_tg, subparsers, pickle_pure_python, genshi_text, meteor_contest, unpickle_pure_python, docutils, pathlib, bench_thread_pool, shortest_path, async_tree_io_tg, many_optionals, sphinx, pprint_pformat, json_loads, scimark_fft, python_startup, scimark_sparse_mat_mult, async_tree_memoization, sqlalchemy_imperative, connected_components, pylint, async_tree_none, async_tree_none_tg, xml_etree_parse, pycparser, async_tree_memoization_tg, sqlite_synth

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 97.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x