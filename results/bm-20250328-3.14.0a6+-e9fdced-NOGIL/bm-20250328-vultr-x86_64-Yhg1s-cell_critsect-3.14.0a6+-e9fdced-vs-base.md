# Results vs. base

- fork: Yhg1s
- ref: cell_critsect
- machine: linux-x86_64
- commit hash: e9fdced
- commit date: 2025-03-28
- overall geometric mean: 1.003x faster
- HPT reliability: 95.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| docutils       | 2.79 sec                                                               | 2.77 sec: 1.01x faster                                         |
| sphinx         | 1.10 sec                                                               | 1.09 sec: 1.00x faster                                         |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_memoization     | 333 ms                                                                 | 334 ms: 1.01x slower                                           |
| async_tree_memoization_tg  | 301 ms                                                                 | 303 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 488 ms: 1.01x slower                                           |
| async_generators           | 381 ms                                                                 | 385 ms: 1.01x slower                                           |
| coroutines                 | 24.0 ms                                                                | 24.3 ms: 1.01x slower                                          |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 525 ms: 1.01x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                   |

Benchmark hidden because not significant (5): async_tree_io, asyncio_websockets, async_tree_none_tg, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 189 ms: 1.10x faster                                           |
| float          | 76.9 ms                                                                | 77.2 ms: 1.00x slower                                          |
| nbody          | 131 ms                                                                 | 138 ms: 1.05x slower                                           |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 2.77 ms                                                                | 2.67 ms: 1.04x faster                                          |
| regex_compile  | 159 ms                                                                 | 158 ms: 1.01x faster                                           |
| regex_v8       | 21.6 ms                                                                | 21.9 ms: 1.01x slower                                          |
| regex_dna      | 169 ms                                                                 | 175 ms: 1.03x slower                                           |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| unpickle_pure_python | 262 us                                                                 | 256 us: 1.02x faster                                           |
| json_dumps           | 12.9 ms                                                                | 12.6 ms: 1.02x faster                                          |
| pickle_pure_python   | 365 us                                                                 | 360 us: 1.01x faster                                           |
| xml_etree_process    | 71.0 ms                                                                | 70.3 ms: 1.01x faster                                          |
| xml_etree_generate   | 97.4 ms                                                                | 96.5 ms: 1.01x faster                                          |
| xml_etree_iterparse  | 88.9 ms                                                                | 88.2 ms: 1.01x faster                                          |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                   |

Benchmark hidden because not significant (3): tomli_loads, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                          |
| python_startup         | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                          |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| mako           | 16.1 ms                                                                | 15.7 ms: 1.03x faster                                          |
| genshi_xml     | 60.2 ms                                                                | 60.7 ms: 1.01x slower                                          |
| genshi_text    | 28.3 ms                                                                | 28.7 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits                   | 207 ms                                                                 | 189 ms: 1.10x faster                                           |
| regex_effbot               | 2.77 ms                                                                | 2.67 ms: 1.04x faster                                          |
| meteor_contest             | 132 ms                                                                 | 129 ms: 1.03x faster                                           |
| logging_format             | 8.49 us                                                                | 8.27 us: 1.03x faster                                          |
| mako                       | 16.1 ms                                                                | 15.7 ms: 1.03x faster                                          |
| unpickle_pure_python       | 262 us                                                                 | 256 us: 1.02x faster                                           |
| mdp                        | 2.74 sec                                                               | 2.68 sec: 1.02x faster                                         |
| logging_simple             | 7.44 us                                                                | 7.27 us: 1.02x faster                                          |
| json_dumps                 | 12.9 ms                                                                | 12.6 ms: 1.02x faster                                          |
| sqlglot_v2_normalize       | 123 ms                                                                 | 120 ms: 1.02x faster                                           |
| hexiom                     | 7.72 ms                                                                | 7.59 ms: 1.02x faster                                          |
| deepcopy                   | 315 us                                                                 | 310 us: 1.02x faster                                           |
| deepcopy_reduce            | 3.25 us                                                                | 3.20 us: 1.02x faster                                          |
| pathlib                    | 19.9 ms                                                                | 19.6 ms: 1.01x faster                                          |
| pickle_pure_python         | 365 us                                                                 | 360 us: 1.01x faster                                           |
| scimark_lu                 | 145 ms                                                                 | 143 ms: 1.01x faster                                           |
| fannkuch                   | 499 ms                                                                 | 493 ms: 1.01x faster                                           |
| spectral_norm              | 114 ms                                                                 | 113 ms: 1.01x faster                                           |
| nqueens                    | 98.8 ms                                                                | 97.7 ms: 1.01x faster                                          |
| sqlglot_v2_parse           | 1.61 ms                                                                | 1.59 ms: 1.01x faster                                          |
| scimark_sor                | 138 ms                                                                 | 137 ms: 1.01x faster                                           |
| xml_etree_process          | 71.0 ms                                                                | 70.3 ms: 1.01x faster                                          |
| xml_etree_generate         | 97.4 ms                                                                | 96.5 ms: 1.01x faster                                          |
| bpe_tokeniser              | 4.85 sec                                                               | 4.81 sec: 1.01x faster                                         |
| sympy_str                  | 338 ms                                                                 | 335 ms: 1.01x faster                                           |
| docutils                   | 2.79 sec                                                               | 2.77 sec: 1.01x faster                                         |
| pprint_safe_repr           | 837 ms                                                                 | 830 ms: 1.01x faster                                           |
| xml_etree_iterparse        | 88.9 ms                                                                | 88.2 ms: 1.01x faster                                          |
| thrift                     | 874 us                                                                 | 868 us: 1.01x faster                                           |
| logging_silent             | 115 ns                                                                 | 114 ns: 1.01x faster                                           |
| sqlglot_v2_optimize        | 61.5 ms                                                                | 61.1 ms: 1.01x faster                                          |
| richards                   | 55.6 ms                                                                | 55.3 ms: 1.01x faster                                          |
| regex_compile              | 159 ms                                                                 | 158 ms: 1.01x faster                                           |
| pprint_pformat             | 1.74 sec                                                               | 1.73 sec: 1.01x faster                                         |
| sphinx                     | 1.10 sec                                                               | 1.09 sec: 1.00x faster                                         |
| deltablue                  | 3.92 ms                                                                | 3.91 ms: 1.00x faster                                          |
| richards_super             | 64.4 ms                                                                | 64.2 ms: 1.00x faster                                          |
| comprehensions             | 21.0 us                                                                | 21.0 us: 1.00x faster                                          |
| bench_thread_pool          | 3.17 ms                                                                | 3.16 ms: 1.00x faster                                          |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                          |
| python_startup             | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                          |
| scimark_fft                | 396 ms                                                                 | 397 ms: 1.00x slower                                           |
| chaos                      | 69.3 ms                                                                | 69.5 ms: 1.00x slower                                          |
| float                      | 76.9 ms                                                                | 77.2 ms: 1.00x slower                                          |
| async_tree_memoization     | 333 ms                                                                 | 334 ms: 1.01x slower                                           |
| genshi_xml                 | 60.2 ms                                                                | 60.7 ms: 1.01x slower                                          |
| async_tree_memoization_tg  | 301 ms                                                                 | 303 ms: 1.01x slower                                           |
| json                       | 5.07 ms                                                                | 5.11 ms: 1.01x slower                                          |
| deepcopy_memo              | 39.2 us                                                                | 39.6 us: 1.01x slower                                          |
| raytrace                   | 328 ms                                                                 | 332 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 488 ms: 1.01x slower                                           |
| async_generators           | 381 ms                                                                 | 385 ms: 1.01x slower                                           |
| coroutines                 | 24.0 ms                                                                | 24.3 ms: 1.01x slower                                          |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 525 ms: 1.01x slower                                           |
| genshi_text                | 28.3 ms                                                                | 28.7 ms: 1.01x slower                                          |
| regex_v8                   | 21.6 ms                                                                | 21.9 ms: 1.01x slower                                          |
| scimark_sparse_mat_mult    | 5.66 ms                                                                | 5.78 ms: 1.02x slower                                          |
| typing_runtime_protocols   | 196 us                                                                 | 201 us: 1.03x slower                                           |
| regex_dna                  | 169 ms                                                                 | 175 ms: 1.03x slower                                           |
| nbody                      | 131 ms                                                                 | 138 ms: 1.05x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (36): subparsers, sqlite_synth, sqlglot_v2_transpile, pycparser, scimark_monte_carlo, sqlalchemy_imperative, dulwich_log, tomli_loads, async_tree_io, xml_etree_parse, crypto_pyaes, sympy_integrate, json_loads, many_optionals, coverage, sympy_sum, sqlalchemy_declarative, pylint, go, django_template, create_gc_cycles, pyflate, bench_mp_pool, k_core, generators, asyncio_websockets, shortest_path, gc_traversal, 2to3, html5lib, sympy_expand, connected_components, telco, async_tree_none_tg, async_tree_io_tg, async_tree_none

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 95.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x