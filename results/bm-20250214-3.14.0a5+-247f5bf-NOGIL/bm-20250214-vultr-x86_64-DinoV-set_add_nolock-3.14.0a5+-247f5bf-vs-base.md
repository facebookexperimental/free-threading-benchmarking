# Results vs. base

- fork: DinoV
- ref: set_add_nolock
- machine: linux-x86_64
- commit hash: 247f5bf
- commit date: 2025-02-14
- overall geometric mean: 1.001x faster
- HPT reliability: 85.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none           | 290 ms                                                                 | 286 ms: 1.01x faster                                            |
| async_tree_memoization    | 355 ms                                                                 | 351 ms: 1.01x faster                                            |
| async_tree_memoization_tg | 322 ms                                                                 | 319 ms: 1.01x faster                                            |
| async_generators          | 370 ms                                                                 | 372 ms: 1.00x slower                                            |
| coroutines                | 23.3 ms                                                                | 23.4 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed   | 535 ms                                                                 | 538 ms: 1.01x slower                                            |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                    |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_io, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| nbody          | 130 ms                                                                 | 129 ms: 1.01x faster                                            |
| float          | 75.4 ms                                                                | 76.0 ms: 1.01x slower                                           |
| pidigits       | 199 ms                                                                 | 213 ms: 1.07x slower                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                 | 182 ms: 1.02x faster                                            |
| regex_effbot   | 2.86 ms                                                                | 2.86 ms: 1.00x faster                                           |
| regex_compile  | 152 ms                                                                 | 152 ms: 1.01x slower                                            |
| regex_v8       | 23.8 ms                                                                | 24.1 ms: 1.01x slower                                           |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_process    | 70.4 ms                                                                | 69.7 ms: 1.01x faster                                           |
| unpickle_pure_python | 252 us                                                                 | 250 us: 1.01x faster                                            |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                            |
| json_dumps           | 12.9 ms                                                                | 12.8 ms: 1.00x faster                                           |
| xml_etree_generate   | 96.1 ms                                                                | 95.8 ms: 1.00x faster                                           |
| json_loads           | 31.3 us                                                                | 31.5 us: 1.01x slower                                           |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                    |

Benchmark hidden because not significant (3): pickle_pure_python, tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.6 ms: 1.01x faster                                           |
| genshi_xml      | 59.6 ms                                                                | 59.2 ms: 1.01x faster                                           |
| django_template | 42.5 ms                                                                | 42.2 ms: 1.01x faster                                           |
| genshi_text     | 27.8 ms                                                                | 27.9 ms: 1.00x slower                                           |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                    |

All benchmarks:
===============

| Benchmark                 | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| spectral_norm             | 109 ms                                                                 | 106 ms: 1.03x faster                                            |
| logging_silent            | 114 ns                                                                 | 111 ns: 1.03x faster                                            |
| sqlite_synth              | 2.06 us                                                                | 2.02 us: 1.02x faster                                           |
| telco                     | 8.66 ms                                                                | 8.48 ms: 1.02x faster                                           |
| scimark_lu                | 138 ms                                                                 | 136 ms: 1.02x faster                                            |
| comprehensions            | 20.0 us                                                                | 19.7 us: 1.02x faster                                           |
| regex_dna                 | 185 ms                                                                 | 182 ms: 1.02x faster                                            |
| scimark_sor               | 133 ms                                                                 | 131 ms: 1.02x faster                                            |
| deepcopy_memo             | 38.4 us                                                                | 37.9 us: 1.01x faster                                           |
| nbody                     | 130 ms                                                                 | 129 ms: 1.01x faster                                            |
| nqueens                   | 97.0 ms                                                                | 95.9 ms: 1.01x faster                                           |
| coverage                  | 96.4 ms                                                                | 95.3 ms: 1.01x faster                                           |
| async_tree_none           | 290 ms                                                                 | 286 ms: 1.01x faster                                            |
| deltablue                 | 3.91 ms                                                                | 3.87 ms: 1.01x faster                                           |
| async_tree_memoization    | 355 ms                                                                 | 351 ms: 1.01x faster                                            |
| xml_etree_process         | 70.4 ms                                                                | 69.7 ms: 1.01x faster                                           |
| scimark_fft               | 389 ms                                                                 | 385 ms: 1.01x faster                                            |
| unpickle_pure_python      | 252 us                                                                 | 250 us: 1.01x faster                                            |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.01x faster                                            |
| pyflate                   | 494 ms                                                                 | 489 ms: 1.01x faster                                            |
| generators                | 32.1 ms                                                                | 31.8 ms: 1.01x faster                                           |
| fannkuch                  | 489 ms                                                                 | 485 ms: 1.01x faster                                            |
| richards                  | 56.6 ms                                                                | 56.1 ms: 1.01x faster                                           |
| crypto_pyaes              | 88.9 ms                                                                | 88.2 ms: 1.01x faster                                           |
| gc_traversal              | 1.74 ms                                                                | 1.73 ms: 1.01x faster                                           |
| create_gc_cycles          | 1.39 ms                                                                | 1.38 ms: 1.01x faster                                           |
| mako                      | 15.8 ms                                                                | 15.6 ms: 1.01x faster                                           |
| async_tree_memoization_tg | 322 ms                                                                 | 319 ms: 1.01x faster                                            |
| scimark_monte_carlo       | 83.8 ms                                                                | 83.2 ms: 1.01x faster                                           |
| pprint_safe_repr          | 823 ms                                                                 | 817 ms: 1.01x faster                                            |
| genshi_xml                | 59.6 ms                                                                | 59.2 ms: 1.01x faster                                           |
| django_template           | 42.5 ms                                                                | 42.2 ms: 1.01x faster                                           |
| chaos                     | 69.6 ms                                                                | 69.2 ms: 1.01x faster                                           |
| shortest_path             | 548 ms                                                                 | 544 ms: 1.01x faster                                            |
| richards_super            | 65.3 ms                                                                | 65.0 ms: 1.01x faster                                           |
| json_dumps                | 12.9 ms                                                                | 12.8 ms: 1.00x faster                                           |
| raytrace                  | 326 ms                                                                 | 325 ms: 1.00x faster                                            |
| xml_etree_generate        | 96.1 ms                                                                | 95.8 ms: 1.00x faster                                           |
| regex_effbot              | 2.86 ms                                                                | 2.86 ms: 1.00x faster                                           |
| genshi_text               | 27.8 ms                                                                | 27.9 ms: 1.00x slower                                           |
| sqlalchemy_declarative    | 157 ms                                                                 | 158 ms: 1.00x slower                                            |
| async_generators          | 370 ms                                                                 | 372 ms: 1.00x slower                                            |
| many_optionals            | 1.17 ms                                                                | 1.18 ms: 1.00x slower                                           |
| coroutines                | 23.3 ms                                                                | 23.4 ms: 1.01x slower                                           |
| regex_compile             | 152 ms                                                                 | 152 ms: 1.01x slower                                            |
| k_core                    | 2.31 sec                                                               | 2.33 sec: 1.01x slower                                          |
| json_loads                | 31.3 us                                                                | 31.5 us: 1.01x slower                                           |
| async_tree_cpu_io_mixed   | 535 ms                                                                 | 538 ms: 1.01x slower                                            |
| sqlglot_normalize         | 120 ms                                                                 | 121 ms: 1.01x slower                                            |
| pathlib                   | 19.0 ms                                                                | 19.2 ms: 1.01x slower                                           |
| float                     | 75.4 ms                                                                | 76.0 ms: 1.01x slower                                           |
| dulwich_log               | 82.0 ms                                                                | 82.8 ms: 1.01x slower                                           |
| regex_v8                  | 23.8 ms                                                                | 24.1 ms: 1.01x slower                                           |
| bpe_tokeniser             | 4.63 sec                                                               | 4.68 sec: 1.01x slower                                          |
| subparsers                | 25.3 ms                                                                | 25.7 ms: 1.01x slower                                           |
| mdp                       | 2.72 sec                                                               | 2.77 sec: 1.02x slower                                          |
| thrift                    | 887 us                                                                 | 903 us: 1.02x slower                                            |
| logging_format            | 8.06 us                                                                | 8.24 us: 1.02x slower                                           |
| logging_simple            | 7.09 us                                                                | 7.27 us: 1.02x slower                                           |
| deepcopy_reduce           | 3.16 us                                                                | 3.25 us: 1.03x slower                                           |
| deepcopy                  | 310 us                                                                 | 320 us: 1.03x slower                                            |
| scimark_sparse_mat_mult   | 5.56 ms                                                                | 5.73 ms: 1.03x slower                                           |
| pidigits                  | 199 ms                                                                 | 213 ms: 1.07x slower                                            |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                    |

Benchmark hidden because not significant (33): async_tree_none_tg, async_tree_io, sqlalchemy_imperative, pickle_pure_python, connected_components, tomli_loads, bench_thread_pool, hexiom, go, sympy_sum, sympy_integrate, xml_etree_iterparse, docutils, html5lib, asyncio_websockets, 2to3, sqlglot_parse, python_startup, python_startup_no_site, sphinx, bench_mp_pool, pylint, async_tree_cpu_io_mixed_tg, async_tree_io_tg, sympy_expand, pycparser, sympy_str, meteor_contest, pprint_pformat, sqlglot_transpile, json, sqlglot_optimize, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 85.35% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x