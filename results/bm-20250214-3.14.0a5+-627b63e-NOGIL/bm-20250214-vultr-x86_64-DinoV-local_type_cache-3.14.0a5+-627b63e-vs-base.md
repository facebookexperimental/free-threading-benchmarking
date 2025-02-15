# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 627b63e
- commit date: 2025-02-14
- overall geometric mean: 1.006x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 307 ms: 1.01x slower                                              |
| html5lib       | 71.2 ms                                                                | 71.6 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| async_tree_memoization_tg  | 322 ms                                                                 | 320 ms: 1.01x faster                                              |
| async_generators           | 370 ms                                                                 | 369 ms: 1.00x faster                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 509 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 542 ms: 1.01x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (6): async_tree_io_tg, asyncio_websockets, async_tree_none, async_tree_memoization, async_tree_io, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 191 ms: 1.04x faster                                              |
| nbody          | 130 ms                                                                 | 133 ms: 1.02x slower                                              |
| float          | 75.4 ms                                                                | 77.1 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                 | 184 ms: 1.01x faster                                              |
| regex_effbot   | 2.86 ms                                                                | 2.87 ms: 1.00x slower                                             |
| regex_compile  | 152 ms                                                                 | 152 ms: 1.01x slower                                              |
| regex_v8       | 23.8 ms                                                                | 25.0 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 252 us                                                                 | 250 us: 1.01x faster                                              |
| json_loads           | 31.3 us                                                                | 31.1 us: 1.01x faster                                             |
| pickle_pure_python   | 364 us                                                                 | 362 us: 1.01x faster                                              |
| xml_etree_process    | 70.4 ms                                                                | 70.3 ms: 1.00x faster                                             |
| xml_etree_iterparse  | 88.2 ms                                                                | 88.8 ms: 1.01x slower                                             |
| tomli_loads          | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                            |
| xml_etree_generate   | 96.1 ms                                                                | 97.0 ms: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.5 ms: 1.01x slower                                             |
| python_startup_no_site | 9.60 ms                                                                | 9.71 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                             |
| django_template | 42.5 ms                                                                | 43.0 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| logging_silent             | 114 ns                                                                 | 110 ns: 1.04x faster                                              |
| pidigits                   | 199 ms                                                                 | 191 ms: 1.04x faster                                              |
| richards                   | 56.6 ms                                                                | 55.7 ms: 1.02x faster                                             |
| meteor_contest             | 129 ms                                                                 | 127 ms: 1.02x faster                                              |
| sqlite_synth               | 2.06 us                                                                | 2.04 us: 1.01x faster                                             |
| scimark_sor                | 133 ms                                                                 | 131 ms: 1.01x faster                                              |
| unpickle_pure_python       | 252 us                                                                 | 250 us: 1.01x faster                                              |
| deltablue                  | 3.91 ms                                                                | 3.88 ms: 1.01x faster                                             |
| regex_dna                  | 185 ms                                                                 | 184 ms: 1.01x faster                                              |
| richards_super             | 65.3 ms                                                                | 64.8 ms: 1.01x faster                                             |
| nqueens                    | 97.0 ms                                                                | 96.3 ms: 1.01x faster                                             |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| async_tree_memoization_tg  | 322 ms                                                                 | 320 ms: 1.01x faster                                              |
| json_loads                 | 31.3 us                                                                | 31.1 us: 1.01x faster                                             |
| pickle_pure_python         | 364 us                                                                 | 362 us: 1.01x faster                                              |
| bench_thread_pool          | 3.34 ms                                                                | 3.32 ms: 1.01x faster                                             |
| mdp                        | 2.72 sec                                                               | 2.71 sec: 1.01x faster                                            |
| create_gc_cycles           | 1.39 ms                                                                | 1.38 ms: 1.00x faster                                             |
| gc_traversal               | 1.74 ms                                                                | 1.74 ms: 1.00x faster                                             |
| scimark_monte_carlo        | 83.8 ms                                                                | 83.6 ms: 1.00x faster                                             |
| async_generators           | 370 ms                                                                 | 369 ms: 1.00x faster                                              |
| sqlalchemy_declarative     | 157 ms                                                                 | 157 ms: 1.00x faster                                              |
| xml_etree_process          | 70.4 ms                                                                | 70.3 ms: 1.00x faster                                             |
| regex_effbot               | 2.86 ms                                                                | 2.87 ms: 1.00x slower                                             |
| k_core                     | 2.31 sec                                                               | 2.32 sec: 1.00x slower                                            |
| fannkuch                   | 489 ms                                                                 | 491 ms: 1.00x slower                                              |
| hexiom                     | 7.38 ms                                                                | 7.40 ms: 1.00x slower                                             |
| go                         | 139 ms                                                                 | 140 ms: 1.00x slower                                              |
| comprehensions             | 20.0 us                                                                | 20.1 us: 1.00x slower                                             |
| bench_mp_pool              | 94.6 ms                                                                | 95.0 ms: 1.00x slower                                             |
| coverage                   | 96.4 ms                                                                | 96.8 ms: 1.00x slower                                             |
| html5lib                   | 71.2 ms                                                                | 71.6 ms: 1.00x slower                                             |
| sqlglot_normalize          | 120 ms                                                                 | 120 ms: 1.00x slower                                              |
| scimark_lu                 | 138 ms                                                                 | 139 ms: 1.01x slower                                              |
| regex_compile              | 152 ms                                                                 | 152 ms: 1.01x slower                                              |
| mako                       | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                             |
| xml_etree_iterparse        | 88.2 ms                                                                | 88.8 ms: 1.01x slower                                             |
| tomli_loads                | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                            |
| deepcopy_memo              | 38.4 us                                                                | 38.7 us: 1.01x slower                                             |
| chaos                      | 69.6 ms                                                                | 70.2 ms: 1.01x slower                                             |
| xml_etree_generate         | 96.1 ms                                                                | 97.0 ms: 1.01x slower                                             |
| 2to3                       | 304 ms                                                                 | 307 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 509 ms: 1.01x slower                                              |
| python_startup             | 15.3 ms                                                                | 15.5 ms: 1.01x slower                                             |
| sqlglot_optimize           | 61.0 ms                                                                | 61.7 ms: 1.01x slower                                             |
| deepcopy_reduce            | 3.16 us                                                                | 3.20 us: 1.01x slower                                             |
| python_startup_no_site     | 9.60 ms                                                                | 9.71 ms: 1.01x slower                                             |
| django_template            | 42.5 ms                                                                | 43.0 ms: 1.01x slower                                             |
| crypto_pyaes               | 88.9 ms                                                                | 90.1 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 542 ms: 1.01x slower                                              |
| bpe_tokeniser              | 4.63 sec                                                               | 4.69 sec: 1.01x slower                                            |
| dulwich_log                | 82.0 ms                                                                | 83.2 ms: 1.01x slower                                             |
| subparsers                 | 25.3 ms                                                                | 25.7 ms: 1.01x slower                                             |
| sympy_sum                  | 185 ms                                                                 | 187 ms: 1.01x slower                                              |
| many_optionals             | 1.17 ms                                                                | 1.19 ms: 1.01x slower                                             |
| pprint_safe_repr           | 823 ms                                                                 | 836 ms: 1.02x slower                                              |
| logging_simple             | 7.09 us                                                                | 7.21 us: 1.02x slower                                             |
| pathlib                    | 19.0 ms                                                                | 19.4 ms: 1.02x slower                                             |
| nbody                      | 130 ms                                                                 | 133 ms: 1.02x slower                                              |
| scimark_fft                | 389 ms                                                                 | 396 ms: 1.02x slower                                              |
| pprint_pformat             | 1.69 sec                                                               | 1.72 sec: 1.02x slower                                            |
| logging_format             | 8.06 us                                                                | 8.21 us: 1.02x slower                                             |
| sympy_integrate            | 24.0 ms                                                                | 24.5 ms: 1.02x slower                                             |
| pycparser                  | 1.19 sec                                                               | 1.21 sec: 1.02x slower                                            |
| spectral_norm              | 109 ms                                                                 | 112 ms: 1.02x slower                                              |
| float                      | 75.4 ms                                                                | 77.1 ms: 1.02x slower                                             |
| sympy_str                  | 332 ms                                                                 | 340 ms: 1.02x slower                                              |
| typing_runtime_protocols   | 197 us                                                                 | 202 us: 1.02x slower                                              |
| sympy_expand               | 542 ms                                                                 | 556 ms: 1.02x slower                                              |
| thrift                     | 887 us                                                                 | 911 us: 1.03x slower                                              |
| sqlglot_parse              | 1.59 ms                                                                | 1.63 ms: 1.03x slower                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 1.97 ms: 1.03x slower                                             |
| pyflate                    | 494 ms                                                                 | 510 ms: 1.03x slower                                              |
| regex_v8                   | 23.8 ms                                                                | 25.0 ms: 1.05x slower                                             |
| scimark_sparse_mat_mult    | 5.56 ms                                                                | 5.94 ms: 1.07x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (21): xml_etree_parse, genshi_xml, json, shortest_path, docutils, async_tree_io_tg, raytrace, asyncio_websockets, async_tree_none, connected_components, async_tree_memoization, deepcopy, async_tree_io, async_tree_none_tg, generators, genshi_text, sphinx, telco, json_dumps, sqlalchemy_imperative, pylint

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x