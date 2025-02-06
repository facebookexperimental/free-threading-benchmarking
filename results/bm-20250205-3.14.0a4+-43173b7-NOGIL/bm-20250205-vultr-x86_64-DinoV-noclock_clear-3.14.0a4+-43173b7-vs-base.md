# Results vs. base

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: 43173b7
- commit date: 2025-02-05
- overall geometric mean: 1.001x slower
- HPT reliability: 83.48%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| docutils       | 2.79 sec                                                               | 2.78 sec: 1.01x faster                                         |
| html5lib       | 70.4 ms                                                                | 68.5 ms: 1.03x faster                                          |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                   |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none            | 286 ms                                                                 | 288 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 502 ms: 1.01x slower                                           |
| async_generators           | 376 ms                                                                 | 379 ms: 1.01x slower                                           |
| async_tree_memoization     | 349 ms                                                                 | 352 ms: 1.01x slower                                           |
| async_tree_io_tg           | 569 ms                                                                 | 575 ms: 1.01x slower                                           |
| coroutines                 | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                          |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 536 ms: 1.01x slower                                           |
| async_tree_io              | 601 ms                                                                 | 610 ms: 1.02x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                   |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 190 ms: 1.09x faster                                           |
| nbody          | 132 ms                                                                 | 134 ms: 1.01x slower                                           |
| float          | 75.2 ms                                                                | 77.3 ms: 1.03x slower                                          |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                          |
| regex_compile  | 149 ms                                                                 | 147 ms: 1.01x faster                                           |
| regex_dna      | 179 ms                                                                 | 177 ms: 1.01x faster                                           |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                   |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_generate   | 96.3 ms                                                                | 96.0 ms: 1.00x faster                                          |
| xml_etree_process    | 68.9 ms                                                                | 68.7 ms: 1.00x faster                                          |
| json_dumps           | 12.8 ms                                                                | 12.8 ms: 1.00x faster                                          |
| xml_etree_iterparse  | 87.0 ms                                                                | 87.5 ms: 1.01x slower                                          |
| unpickle_pure_python | 244 us                                                                 | 245 us: 1.01x slower                                           |
| xml_etree_parse      | 126 ms                                                                 | 128 ms: 1.01x slower                                           |
| pickle_pure_python   | 364 us                                                                 | 370 us: 1.02x slower                                           |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                   |

Benchmark hidden because not significant (2): tomli_loads, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                          |
| python_startup_no_site | 9.60 ms                                                                | 9.64 ms: 1.00x slower                                          |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                          |
| genshi_text     | 27.4 ms                                                                | 27.7 ms: 1.01x slower                                          |
| django_template | 42.2 ms                                                                | 42.8 ms: 1.01x slower                                          |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                   |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits                   | 207 ms                                                                 | 190 ms: 1.09x faster                                           |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.43 ms: 1.04x faster                                          |
| nqueens                    | 99.9 ms                                                                | 96.6 ms: 1.03x faster                                          |
| create_gc_cycles           | 1.37 ms                                                                | 1.33 ms: 1.03x faster                                          |
| regex_effbot               | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                          |
| html5lib                   | 70.4 ms                                                                | 68.5 ms: 1.03x faster                                          |
| mdp                        | 2.76 sec                                                               | 2.70 sec: 1.02x faster                                         |
| deltablue                  | 4.60 ms                                                                | 4.52 ms: 1.02x faster                                          |
| regex_compile              | 149 ms                                                                 | 147 ms: 1.01x faster                                           |
| deepcopy_memo              | 38.0 us                                                                | 37.6 us: 1.01x faster                                          |
| thrift                     | 914 us                                                                 | 905 us: 1.01x faster                                           |
| meteor_contest             | 130 ms                                                                 | 129 ms: 1.01x faster                                           |
| comprehensions             | 20.0 us                                                                | 19.8 us: 1.01x faster                                          |
| scimark_fft                | 378 ms                                                                 | 374 ms: 1.01x faster                                           |
| regex_dna                  | 179 ms                                                                 | 177 ms: 1.01x faster                                           |
| scimark_monte_carlo        | 81.3 ms                                                                | 80.7 ms: 1.01x faster                                          |
| docutils                   | 2.79 sec                                                               | 2.78 sec: 1.01x faster                                         |
| sympy_sum                  | 185 ms                                                                 | 184 ms: 1.01x faster                                           |
| xml_etree_generate         | 96.3 ms                                                                | 96.0 ms: 1.00x faster                                          |
| xml_etree_process          | 68.9 ms                                                                | 68.7 ms: 1.00x faster                                          |
| raytrace                   | 319 ms                                                                 | 318 ms: 1.00x faster                                           |
| json_dumps                 | 12.8 ms                                                                | 12.8 ms: 1.00x faster                                          |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                          |
| sympy_integrate            | 23.9 ms                                                                | 24.0 ms: 1.00x slower                                          |
| python_startup_no_site     | 9.60 ms                                                                | 9.64 ms: 1.00x slower                                          |
| sympy_str                  | 332 ms                                                                 | 334 ms: 1.00x slower                                           |
| mako                       | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                          |
| xml_etree_iterparse        | 87.0 ms                                                                | 87.5 ms: 1.01x slower                                          |
| pprint_pformat             | 1.69 sec                                                               | 1.70 sec: 1.01x slower                                         |
| unpickle_pure_python       | 244 us                                                                 | 245 us: 1.01x slower                                           |
| sqlalchemy_declarative     | 156 ms                                                                 | 157 ms: 1.01x slower                                           |
| many_optionals             | 1.17 ms                                                                | 1.18 ms: 1.01x slower                                          |
| async_tree_none            | 286 ms                                                                 | 288 ms: 1.01x slower                                           |
| fannkuch                   | 480 ms                                                                 | 483 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 502 ms: 1.01x slower                                           |
| hexiom                     | 7.29 ms                                                                | 7.35 ms: 1.01x slower                                          |
| async_generators           | 376 ms                                                                 | 379 ms: 1.01x slower                                           |
| async_tree_memoization     | 349 ms                                                                 | 352 ms: 1.01x slower                                           |
| subparsers                 | 25.5 ms                                                                | 25.7 ms: 1.01x slower                                          |
| nbody                      | 132 ms                                                                 | 134 ms: 1.01x slower                                           |
| logging_format             | 8.09 us                                                                | 8.16 us: 1.01x slower                                          |
| async_tree_io_tg           | 569 ms                                                                 | 575 ms: 1.01x slower                                           |
| bpe_tokeniser              | 4.62 sec                                                               | 4.67 sec: 1.01x slower                                         |
| coroutines                 | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                          |
| scimark_sor                | 130 ms                                                                 | 131 ms: 1.01x slower                                           |
| sqlglot_transpile          | 1.88 ms                                                                | 1.90 ms: 1.01x slower                                          |
| go                         | 134 ms                                                                 | 136 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 536 ms: 1.01x slower                                           |
| xml_etree_parse            | 126 ms                                                                 | 128 ms: 1.01x slower                                           |
| deepcopy                   | 309 us                                                                 | 313 us: 1.01x slower                                           |
| genshi_text                | 27.4 ms                                                                | 27.7 ms: 1.01x slower                                          |
| scimark_lu                 | 135 ms                                                                 | 137 ms: 1.01x slower                                           |
| django_template            | 42.2 ms                                                                | 42.8 ms: 1.01x slower                                          |
| pickle_pure_python         | 364 us                                                                 | 370 us: 1.02x slower                                           |
| spectral_norm              | 106 ms                                                                 | 108 ms: 1.02x slower                                           |
| async_tree_io              | 601 ms                                                                 | 610 ms: 1.02x slower                                           |
| crypto_pyaes               | 86.3 ms                                                                | 87.8 ms: 1.02x slower                                          |
| float                      | 75.2 ms                                                                | 77.3 ms: 1.03x slower                                          |
| pyflate                    | 484 ms                                                                 | 498 ms: 1.03x slower                                           |
| logging_silent             | 109 ns                                                                 | 112 ns: 1.03x slower                                           |
| gc_traversal               | 1.62 ms                                                                | 1.76 ms: 1.09x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                   |

Benchmark hidden because not significant (35): json, richards_super, connected_components, sphinx, regex_v8, telco, generators, richards, pprint_safe_repr, tomli_loads, k_core, sqlglot_optimize, typing_runtime_protocols, chaos, bench_mp_pool, sqlglot_normalize, json_loads, pycparser, 2to3, dulwich_log, bench_thread_pool, asyncio_websockets, async_tree_none_tg, deepcopy_reduce, sqlglot_parse, coverage, pathlib, sympy_expand, logging_simple, async_tree_memoization_tg, pylint, shortest_path, genshi_xml, sqlite_synth, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 83.48% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x