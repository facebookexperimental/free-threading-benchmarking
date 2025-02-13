# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 1b02bc2
- commit date: 2025-02-12
- overall geometric mean: 1.002x faster
- HPT reliability: 95.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| docutils       | 2.84 sec                                                               | 2.83 sec: 1.00x faster                                            |
| html5lib       | 72.4 ms                                                                | 71.8 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_memoization     | 355 ms                                                                 | 352 ms: 1.01x faster                                              |
| async_tree_io              | 612 ms                                                                 | 608 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 509 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 533 ms                                                                 | 541 ms: 1.02x slower                                              |
| async_generators           | 370 ms                                                                 | 376 ms: 1.02x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (6): async_tree_none, async_tree_memoization_tg, asyncio_websockets, async_tree_io_tg, coroutines, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 132 ms                                                                 | 131 ms: 1.01x faster                                              |
| pidigits       | 195 ms                                                                 | 203 ms: 1.04x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.74 ms: 1.04x faster                                             |
| regex_dna      | 182 ms                                                                 | 180 ms: 1.01x faster                                              |
| regex_compile  | 152 ms                                                                 | 151 ms: 1.01x faster                                              |
| regex_v8       | 23.9 ms                                                                | 23.8 ms: 1.00x faster                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads           | 31.5 us                                                                | 31.0 us: 1.02x faster                                             |
| xml_etree_process    | 68.6 ms                                                                | 68.1 ms: 1.01x faster                                             |
| json_dumps           | 12.8 ms                                                                | 12.8 ms: 1.01x faster                                             |
| unpickle_pure_python | 248 us                                                                 | 247 us: 1.01x faster                                              |
| xml_etree_generate   | 96.7 ms                                                                | 96.3 ms: 1.00x faster                                             |
| tomli_loads          | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                            |
| xml_etree_iterparse  | 87.7 ms                                                                | 88.3 ms: 1.01x slower                                             |
| pickle_pure_python   | 369 us                                                                 | 372 us: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.62 ms                                                                | 9.63 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 42.3 ms                                                                | 41.7 ms: 1.01x faster                                             |
| genshi_xml      | 59.7 ms                                                                | 58.9 ms: 1.01x faster                                             |
| mako            | 15.7 ms                                                                | 15.8 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| logging_silent             | 114 ns                                                                 | 110 ns: 1.04x faster                                              |
| regex_effbot               | 2.84 ms                                                                | 2.74 ms: 1.04x faster                                             |
| pyflate                    | 509 ms                                                                 | 493 ms: 1.03x faster                                              |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.02x faster                                              |
| deepcopy_memo              | 38.4 us                                                                | 37.6 us: 1.02x faster                                             |
| telco                      | 8.63 ms                                                                | 8.45 ms: 1.02x faster                                             |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.02x faster                                              |
| json_loads                 | 31.5 us                                                                | 31.0 us: 1.02x faster                                             |
| pathlib                    | 19.4 ms                                                                | 19.1 ms: 1.01x faster                                             |
| django_template            | 42.3 ms                                                                | 41.7 ms: 1.01x faster                                             |
| genshi_xml                 | 59.7 ms                                                                | 58.9 ms: 1.01x faster                                             |
| sqlalchemy_imperative      | 24.6 ms                                                                | 24.3 ms: 1.01x faster                                             |
| typing_runtime_protocols   | 200 us                                                                 | 197 us: 1.01x faster                                              |
| pprint_safe_repr           | 825 ms                                                                 | 815 ms: 1.01x faster                                              |
| deepcopy                   | 309 us                                                                 | 305 us: 1.01x faster                                              |
| hexiom                     | 7.44 ms                                                                | 7.36 ms: 1.01x faster                                             |
| sympy_expand               | 552 ms                                                                 | 546 ms: 1.01x faster                                              |
| sympy_str                  | 338 ms                                                                 | 334 ms: 1.01x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 352 ms: 1.01x faster                                              |
| regex_dna                  | 182 ms                                                                 | 180 ms: 1.01x faster                                              |
| logging_simple             | 7.22 us                                                                | 7.15 us: 1.01x faster                                             |
| nbody                      | 132 ms                                                                 | 131 ms: 1.01x faster                                              |
| go                         | 140 ms                                                                 | 139 ms: 1.01x faster                                              |
| thrift                     | 908 us                                                                 | 901 us: 1.01x faster                                              |
| regex_compile              | 152 ms                                                                 | 151 ms: 1.01x faster                                              |
| html5lib                   | 72.4 ms                                                                | 71.8 ms: 1.01x faster                                             |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.01x faster                                             |
| xml_etree_process          | 68.6 ms                                                                | 68.1 ms: 1.01x faster                                             |
| fannkuch                   | 493 ms                                                                 | 490 ms: 1.01x faster                                              |
| pprint_pformat             | 1.70 sec                                                               | 1.69 sec: 1.01x faster                                            |
| raytrace                   | 330 ms                                                                 | 328 ms: 1.01x faster                                              |
| richards_super             | 65.7 ms                                                                | 65.3 ms: 1.01x faster                                             |
| json_dumps                 | 12.8 ms                                                                | 12.8 ms: 1.01x faster                                             |
| unpickle_pure_python       | 248 us                                                                 | 247 us: 1.01x faster                                              |
| async_tree_io              | 612 ms                                                                 | 608 ms: 1.01x faster                                              |
| xml_etree_generate         | 96.7 ms                                                                | 96.3 ms: 1.00x faster                                             |
| docutils                   | 2.84 sec                                                               | 2.83 sec: 1.00x faster                                            |
| regex_v8                   | 23.9 ms                                                                | 23.8 ms: 1.00x faster                                             |
| sympy_integrate            | 24.1 ms                                                                | 24.1 ms: 1.00x faster                                             |
| comprehensions             | 20.0 us                                                                | 19.9 us: 1.00x faster                                             |
| python_startup_no_site     | 9.62 ms                                                                | 9.63 ms: 1.00x slower                                             |
| bpe_tokeniser              | 4.67 sec                                                               | 4.69 sec: 1.00x slower                                            |
| mako                       | 15.7 ms                                                                | 15.8 ms: 1.01x slower                                             |
| crypto_pyaes               | 87.3 ms                                                                | 87.8 ms: 1.01x slower                                             |
| tomli_loads                | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                            |
| sqlglot_parse              | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                             |
| xml_etree_iterparse        | 87.7 ms                                                                | 88.3 ms: 1.01x slower                                             |
| generators                 | 31.4 ms                                                                | 31.7 ms: 1.01x slower                                             |
| nqueens                    | 95.4 ms                                                                | 96.1 ms: 1.01x slower                                             |
| pickle_pure_python         | 369 us                                                                 | 372 us: 1.01x slower                                              |
| scimark_fft                | 385 ms                                                                 | 388 ms: 1.01x slower                                              |
| sqlite_synth               | 2.03 us                                                                | 2.05 us: 1.01x slower                                             |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 509 ms: 1.01x slower                                              |
| scimark_monte_carlo        | 82.3 ms                                                                | 83.4 ms: 1.01x slower                                             |
| coverage                   | 96.8 ms                                                                | 98.0 ms: 1.01x slower                                             |
| gc_traversal               | 1.72 ms                                                                | 1.75 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed    | 533 ms                                                                 | 541 ms: 1.02x slower                                              |
| async_generators           | 370 ms                                                                 | 376 ms: 1.02x slower                                              |
| scimark_lu                 | 135 ms                                                                 | 137 ms: 1.02x slower                                              |
| create_gc_cycles           | 1.37 ms                                                                | 1.40 ms: 1.02x slower                                             |
| scimark_sparse_mat_mult    | 5.65 ms                                                                | 5.76 ms: 1.02x slower                                             |
| subparsers                 | 25.4 ms                                                                | 25.9 ms: 1.02x slower                                             |
| mdp                        | 2.70 sec                                                               | 2.76 sec: 1.02x slower                                            |
| pidigits                   | 195 ms                                                                 | 203 ms: 1.04x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (32): async_tree_none, connected_components, sphinx, logging_format, json, deltablue, sqlglot_normalize, dulwich_log, async_tree_memoization_tg, deepcopy_reduce, float, richards, xml_etree_parse, sqlglot_optimize, 2to3, shortest_path, bench_thread_pool, asyncio_websockets, sympy_sum, python_startup, bench_mp_pool, async_tree_io_tg, pycparser, coroutines, sqlalchemy_declarative, k_core, genshi_text, pylint, chaos, meteor_contest, sqlglot_transpile, async_tree_none_tg

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 95.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x