# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: ab974f8
- commit date: 2025-02-18
- overall geometric mean: 1.006x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 307 ms: 1.01x slower                                              |
| docutils       | 2.80 sec                                                               | 2.78 sec: 1.01x faster                                            |
| html5lib       | 71.2 ms                                                                | 73.4 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 507 ms: 1.01x slower                                              |
| async_generators           | 370 ms                                                                 | 373 ms: 1.01x slower                                              |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| async_tree_memoization     | 355 ms                                                                 | 359 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 543 ms: 1.02x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (6): asyncio_websockets, async_tree_memoization_tg, async_tree_io_tg, async_tree_io, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 191 ms: 1.04x faster                                              |
| nbody          | 130 ms                                                                 | 130 ms: 1.01x faster                                              |
| float          | 75.4 ms                                                                | 78.4 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                 | 182 ms: 1.02x faster                                              |
| regex_effbot   | 2.86 ms                                                                | 2.81 ms: 1.02x faster                                             |
| regex_v8       | 23.8 ms                                                                | 23.7 ms: 1.01x faster                                             |
| regex_compile  | 152 ms                                                                 | 152 ms: 1.00x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 252 us                                                                 | 249 us: 1.01x faster                                              |
| pickle_pure_python   | 364 us                                                                 | 360 us: 1.01x faster                                              |
| json_loads           | 31.3 us                                                                | 31.0 us: 1.01x faster                                             |
| xml_etree_process    | 70.4 ms                                                                | 70.1 ms: 1.00x faster                                             |
| tomli_loads          | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                            |
| xml_etree_generate   | 96.1 ms                                                                | 96.8 ms: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.60 ms                                                                | 9.74 ms: 1.01x slower                                             |
| python_startup         | 15.3 ms                                                                | 15.5 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                             |
| genshi_xml      | 59.6 ms                                                                | 60.1 ms: 1.01x slower                                             |
| django_template | 42.5 ms                                                                | 43.0 ms: 1.01x slower                                             |
| genshi_text     | 27.8 ms                                                                | 28.2 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mdp                        | 2.72 sec                                                               | 2.59 sec: 1.05x faster                                            |
| pidigits                   | 199 ms                                                                 | 191 ms: 1.04x faster                                              |
| regex_dna                  | 185 ms                                                                 | 182 ms: 1.02x faster                                              |
| logging_silent             | 114 ns                                                                 | 112 ns: 1.02x faster                                              |
| regex_effbot               | 2.86 ms                                                                | 2.81 ms: 1.02x faster                                             |
| telco                      | 8.66 ms                                                                | 8.51 ms: 1.02x faster                                             |
| unpickle_pure_python       | 252 us                                                                 | 249 us: 1.01x faster                                              |
| pickle_pure_python         | 364 us                                                                 | 360 us: 1.01x faster                                              |
| scimark_monte_carlo        | 83.8 ms                                                                | 83.1 ms: 1.01x faster                                             |
| deepcopy_reduce            | 3.16 us                                                                | 3.14 us: 1.01x faster                                             |
| json_loads                 | 31.3 us                                                                | 31.0 us: 1.01x faster                                             |
| regex_v8                   | 23.8 ms                                                                | 23.7 ms: 1.01x faster                                             |
| docutils                   | 2.80 sec                                                               | 2.78 sec: 1.01x faster                                            |
| crypto_pyaes               | 88.9 ms                                                                | 88.4 ms: 1.01x faster                                             |
| nqueens                    | 97.0 ms                                                                | 96.5 ms: 1.01x faster                                             |
| nbody                      | 130 ms                                                                 | 130 ms: 1.01x faster                                              |
| scimark_sor                | 133 ms                                                                 | 132 ms: 1.01x faster                                              |
| mako                       | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                             |
| xml_etree_process          | 70.4 ms                                                                | 70.1 ms: 1.00x faster                                             |
| hexiom                     | 7.38 ms                                                                | 7.40 ms: 1.00x slower                                             |
| k_core                     | 2.31 sec                                                               | 2.32 sec: 1.00x slower                                            |
| pprint_safe_repr           | 823 ms                                                                 | 826 ms: 1.00x slower                                              |
| regex_compile              | 152 ms                                                                 | 152 ms: 1.00x slower                                              |
| richards_super             | 65.3 ms                                                                | 65.6 ms: 1.00x slower                                             |
| gc_traversal               | 1.74 ms                                                                | 1.75 ms: 1.01x slower                                             |
| pprint_pformat             | 1.69 sec                                                               | 1.70 sec: 1.01x slower                                            |
| chaos                      | 69.6 ms                                                                | 70.0 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 507 ms: 1.01x slower                                              |
| tomli_loads                | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                            |
| xml_etree_generate         | 96.1 ms                                                                | 96.8 ms: 1.01x slower                                             |
| genshi_xml                 | 59.6 ms                                                                | 60.1 ms: 1.01x slower                                             |
| spectral_norm              | 109 ms                                                                 | 110 ms: 1.01x slower                                              |
| fannkuch                   | 489 ms                                                                 | 494 ms: 1.01x slower                                              |
| async_generators           | 370 ms                                                                 | 373 ms: 1.01x slower                                              |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| go                         | 139 ms                                                                 | 141 ms: 1.01x slower                                              |
| coverage                   | 96.4 ms                                                                | 97.4 ms: 1.01x slower                                             |
| 2to3                       | 304 ms                                                                 | 307 ms: 1.01x slower                                              |
| sqlglot_optimize           | 61.0 ms                                                                | 61.6 ms: 1.01x slower                                             |
| deltablue                  | 3.91 ms                                                                | 3.95 ms: 1.01x slower                                             |
| async_tree_memoization     | 355 ms                                                                 | 359 ms: 1.01x slower                                              |
| scimark_lu                 | 138 ms                                                                 | 140 ms: 1.01x slower                                              |
| bench_mp_pool              | 94.6 ms                                                                | 95.7 ms: 1.01x slower                                             |
| django_template            | 42.5 ms                                                                | 43.0 ms: 1.01x slower                                             |
| pycparser                  | 1.19 sec                                                               | 1.20 sec: 1.01x slower                                            |
| deepcopy                   | 310 us                                                                 | 315 us: 1.01x slower                                              |
| scimark_fft                | 389 ms                                                                 | 395 ms: 1.01x slower                                              |
| dulwich_log                | 82.0 ms                                                                | 83.2 ms: 1.01x slower                                             |
| python_startup_no_site     | 9.60 ms                                                                | 9.74 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 543 ms: 1.02x slower                                              |
| many_optionals             | 1.17 ms                                                                | 1.19 ms: 1.02x slower                                             |
| typing_runtime_protocols   | 197 us                                                                 | 200 us: 1.02x slower                                              |
| python_startup             | 15.3 ms                                                                | 15.5 ms: 1.02x slower                                             |
| subparsers                 | 25.3 ms                                                                | 25.7 ms: 1.02x slower                                             |
| genshi_text                | 27.8 ms                                                                | 28.2 ms: 1.02x slower                                             |
| bpe_tokeniser              | 4.63 sec                                                               | 4.71 sec: 1.02x slower                                            |
| sympy_sum                  | 185 ms                                                                 | 188 ms: 1.02x slower                                              |
| pathlib                    | 19.0 ms                                                                | 19.4 ms: 1.02x slower                                             |
| sqlglot_normalize          | 120 ms                                                                 | 122 ms: 1.02x slower                                              |
| sympy_expand               | 542 ms                                                                 | 554 ms: 1.02x slower                                              |
| sympy_integrate            | 24.0 ms                                                                | 24.6 ms: 1.02x slower                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 1.96 ms: 1.02x slower                                             |
| thrift                     | 887 us                                                                 | 910 us: 1.03x slower                                              |
| logging_format             | 8.06 us                                                                | 8.27 us: 1.03x slower                                             |
| sqlglot_parse              | 1.59 ms                                                                | 1.63 ms: 1.03x slower                                             |
| logging_simple             | 7.09 us                                                                | 7.29 us: 1.03x slower                                             |
| scimark_sparse_mat_mult    | 5.56 ms                                                                | 5.72 ms: 1.03x slower                                             |
| sympy_str                  | 332 ms                                                                 | 342 ms: 1.03x slower                                              |
| html5lib                   | 71.2 ms                                                                | 73.4 ms: 1.03x slower                                             |
| pyflate                    | 494 ms                                                                 | 509 ms: 1.03x slower                                              |
| sqlalchemy_imperative      | 24.2 ms                                                                | 25.1 ms: 1.04x slower                                             |
| float                      | 75.4 ms                                                                | 78.4 ms: 1.04x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (24): json, xml_etree_parse, asyncio_websockets, generators, bench_thread_pool, raytrace, richards, shortest_path, sqlalchemy_declarative, sqlite_synth, comprehensions, xml_etree_iterparse, json_dumps, async_tree_memoization_tg, deepcopy_memo, meteor_contest, create_gc_cycles, async_tree_io_tg, async_tree_io, connected_components, sphinx, async_tree_none, async_tree_none_tg, pylint

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x