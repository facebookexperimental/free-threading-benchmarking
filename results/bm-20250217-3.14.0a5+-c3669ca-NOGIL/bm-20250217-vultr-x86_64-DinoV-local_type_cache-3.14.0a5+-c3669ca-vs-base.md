# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: c3669ca
- commit date: 2025-02-17
- overall geometric mean: 1.014x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 308 ms: 1.01x slower                                              |
| html5lib       | 71.2 ms                                                                | 71.6 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.01x slower                                             |
| async_generators           | 370 ms                                                                 | 379 ms: 1.02x slower                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 554 ms: 1.10x slower                                              |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 589 ms: 1.10x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (7): asyncio_websockets, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg, async_tree_none, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 75.4 ms                                                                | 78.3 ms: 1.04x slower                                             |
| nbody          | 130 ms                                                                 | 137 ms: 1.05x slower                                              |
| pidigits       | 199 ms                                                                 | 219 ms: 1.10x slower                                              |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.80 ms: 1.02x faster                                             |
| regex_v8       | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                             |
| regex_dna      | 185 ms                                                                 | 186 ms: 1.00x slower                                              |
| regex_compile  | 152 ms                                                                 | 153 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 252 us                                                                 | 250 us: 1.01x faster                                              |
| tomli_loads          | 2.34 sec                                                               | 2.35 sec: 1.00x slower                                            |
| json_dumps           | 12.9 ms                                                                | 12.9 ms: 1.00x slower                                             |
| json_loads           | 31.3 us                                                                | 31.5 us: 1.01x slower                                             |
| xml_etree_process    | 70.4 ms                                                                | 70.9 ms: 1.01x slower                                             |
| xml_etree_generate   | 96.1 ms                                                                | 97.6 ms: 1.01x slower                                             |
| xml_etree_iterparse  | 88.2 ms                                                                | 89.6 ms: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.60 ms                                                                | 9.68 ms: 1.01x slower                                             |
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 27.8 ms                                                                | 27.9 ms: 1.00x slower                                             |
| django_template | 42.5 ms                                                                | 43.3 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250214-vultr-x86_64-python-303043f5062c1e7ffb79-3.14.0a5+-303043f | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot               | 2.86 ms                                                                | 2.80 ms: 1.02x faster                                             |
| regex_v8                   | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                             |
| sqlite_synth               | 2.06 us                                                                | 2.04 us: 1.01x faster                                             |
| unpickle_pure_python       | 252 us                                                                 | 250 us: 1.01x faster                                              |
| logging_silent             | 114 ns                                                                 | 115 ns: 1.00x slower                                              |
| tomli_loads                | 2.34 sec                                                               | 2.35 sec: 1.00x slower                                            |
| hexiom                     | 7.38 ms                                                                | 7.41 ms: 1.00x slower                                             |
| regex_dna                  | 185 ms                                                                 | 186 ms: 1.00x slower                                              |
| genshi_text                | 27.8 ms                                                                | 27.9 ms: 1.00x slower                                             |
| json_dumps                 | 12.9 ms                                                                | 12.9 ms: 1.00x slower                                             |
| scimark_monte_carlo        | 83.8 ms                                                                | 84.1 ms: 1.00x slower                                             |
| html5lib                   | 71.2 ms                                                                | 71.6 ms: 1.01x slower                                             |
| k_core                     | 2.31 sec                                                               | 2.33 sec: 1.01x slower                                            |
| bench_mp_pool              | 94.6 ms                                                                | 95.1 ms: 1.01x slower                                             |
| nqueens                    | 97.0 ms                                                                | 97.6 ms: 1.01x slower                                             |
| json_loads                 | 31.3 us                                                                | 31.5 us: 1.01x slower                                             |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.01x slower                                             |
| xml_etree_process          | 70.4 ms                                                                | 70.9 ms: 1.01x slower                                             |
| deepcopy_memo              | 38.4 us                                                                | 38.7 us: 1.01x slower                                             |
| pyflate                    | 494 ms                                                                 | 497 ms: 1.01x slower                                              |
| regex_compile              | 152 ms                                                                 | 153 ms: 1.01x slower                                              |
| python_startup_no_site     | 9.60 ms                                                                | 9.68 ms: 1.01x slower                                             |
| richards                   | 56.6 ms                                                                | 57.1 ms: 1.01x slower                                             |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| scimark_sor                | 133 ms                                                                 | 134 ms: 1.01x slower                                              |
| go                         | 139 ms                                                                 | 141 ms: 1.01x slower                                              |
| fannkuch                   | 489 ms                                                                 | 495 ms: 1.01x slower                                              |
| deepcopy                   | 310 us                                                                 | 314 us: 1.01x slower                                              |
| deepcopy_reduce            | 3.16 us                                                                | 3.20 us: 1.01x slower                                             |
| deltablue                  | 3.91 ms                                                                | 3.96 ms: 1.01x slower                                             |
| richards_super             | 65.3 ms                                                                | 66.2 ms: 1.01x slower                                             |
| 2to3                       | 304 ms                                                                 | 308 ms: 1.01x slower                                              |
| raytrace                   | 326 ms                                                                 | 331 ms: 1.01x slower                                              |
| xml_etree_generate         | 96.1 ms                                                                | 97.6 ms: 1.01x slower                                             |
| typing_runtime_protocols   | 197 us                                                                 | 200 us: 1.02x slower                                              |
| logging_simple             | 7.09 us                                                                | 7.21 us: 1.02x slower                                             |
| coverage                   | 96.4 ms                                                                | 97.9 ms: 1.02x slower                                             |
| xml_etree_iterparse        | 88.2 ms                                                                | 89.6 ms: 1.02x slower                                             |
| pycparser                  | 1.19 sec                                                               | 1.21 sec: 1.02x slower                                            |
| subparsers                 | 25.3 ms                                                                | 25.7 ms: 1.02x slower                                             |
| django_template            | 42.5 ms                                                                | 43.3 ms: 1.02x slower                                             |
| meteor_contest             | 129 ms                                                                 | 131 ms: 1.02x slower                                              |
| many_optionals             | 1.17 ms                                                                | 1.19 ms: 1.02x slower                                             |
| sqlglot_normalize          | 120 ms                                                                 | 122 ms: 1.02x slower                                              |
| thrift                     | 887 us                                                                 | 905 us: 1.02x slower                                              |
| bpe_tokeniser              | 4.63 sec                                                               | 4.72 sec: 1.02x slower                                            |
| sympy_sum                  | 185 ms                                                                 | 189 ms: 1.02x slower                                              |
| spectral_norm              | 109 ms                                                                 | 112 ms: 1.02x slower                                              |
| chaos                      | 69.6 ms                                                                | 71.1 ms: 1.02x slower                                             |
| mdp                        | 2.72 sec                                                               | 2.78 sec: 1.02x slower                                            |
| pprint_safe_repr           | 823 ms                                                                 | 840 ms: 1.02x slower                                              |
| dulwich_log                | 82.0 ms                                                                | 83.9 ms: 1.02x slower                                             |
| sympy_integrate            | 24.0 ms                                                                | 24.6 ms: 1.02x slower                                             |
| pprint_pformat             | 1.69 sec                                                               | 1.73 sec: 1.02x slower                                            |
| comprehensions             | 20.0 us                                                                | 20.5 us: 1.02x slower                                             |
| logging_format             | 8.06 us                                                                | 8.25 us: 1.02x slower                                             |
| async_generators           | 370 ms                                                                 | 379 ms: 1.02x slower                                              |
| sympy_expand               | 542 ms                                                                 | 555 ms: 1.02x slower                                              |
| crypto_pyaes               | 88.9 ms                                                                | 91.2 ms: 1.02x slower                                             |
| sqlglot_optimize           | 61.0 ms                                                                | 62.5 ms: 1.03x slower                                             |
| pathlib                    | 19.0 ms                                                                | 19.5 ms: 1.03x slower                                             |
| sympy_str                  | 332 ms                                                                 | 342 ms: 1.03x slower                                              |
| scimark_lu                 | 138 ms                                                                 | 143 ms: 1.03x slower                                              |
| scimark_fft                | 389 ms                                                                 | 402 ms: 1.03x slower                                              |
| sqlglot_transpile          | 1.91 ms                                                                | 1.98 ms: 1.03x slower                                             |
| sqlglot_parse              | 1.59 ms                                                                | 1.65 ms: 1.04x slower                                             |
| float                      | 75.4 ms                                                                | 78.3 ms: 1.04x slower                                             |
| nbody                      | 130 ms                                                                 | 137 ms: 1.05x slower                                              |
| scimark_sparse_mat_mult    | 5.56 ms                                                                | 5.87 ms: 1.05x slower                                             |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 554 ms: 1.10x slower                                              |
| pidigits                   | 199 ms                                                                 | 219 ms: 1.10x slower                                              |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 589 ms: 1.10x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (24): telco, bench_thread_pool, asyncio_websockets, async_tree_memoization_tg, create_gc_cycles, sqlalchemy_declarative, mako, shortest_path, async_tree_io_tg, async_tree_none_tg, gc_traversal, generators, docutils, async_tree_none, pickle_pure_python, async_tree_memoization, async_tree_io, genshi_xml, xml_etree_parse, json, sphinx, connected_components, sqlalchemy_imperative, pylint

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x