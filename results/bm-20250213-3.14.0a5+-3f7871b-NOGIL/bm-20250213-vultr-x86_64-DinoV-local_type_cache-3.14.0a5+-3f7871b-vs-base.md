# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 3f7871b
- commit date: 2025-02-13
- overall geometric mean: 1.001x faster
- HPT reliability: 54.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 304 ms: 1.00x faster                                              |
| docutils       | 2.83 sec                                                               | 2.80 sec: 1.01x faster                                            |
| html5lib       | 72.0 ms                                                                | 72.9 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 23.7 ms                                                                | 23.3 ms: 1.02x faster                                             |
| async_tree_io              | 611 ms                                                                 | 606 ms: 1.01x faster                                              |
| async_generators           | 375 ms                                                                 | 374 ms: 1.00x faster                                              |
| async_tree_cpu_io_mixed    | 588 ms                                                                 | 591 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                 | 559 ms: 1.01x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_none, async_tree_memoization_tg, asyncio_websockets, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 206 ms: 1.05x faster                                              |
| nbody          | 132 ms                                                                 | 129 ms: 1.02x faster                                              |
| float          | 75.6 ms                                                                | 76.6 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 23.8 ms                                                                | 23.1 ms: 1.03x faster                                             |
| regex_compile  | 151 ms                                                                 | 153 ms: 1.01x slower                                              |
| regex_dna      | 178 ms                                                                 | 185 ms: 1.04x slower                                              |
| regex_effbot   | 2.77 ms                                                                | 2.87 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 365 us                                                                 | 358 us: 1.02x faster                                              |
| unpickle_pure_python | 253 us                                                                 | 249 us: 1.02x faster                                              |
| tomli_loads          | 2.37 sec                                                               | 2.35 sec: 1.01x faster                                            |
| json_dumps           | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                             |
| xml_etree_process    | 70.5 ms                                                                | 70.2 ms: 1.00x faster                                             |
| json_loads           | 31.3 us                                                                | 31.2 us: 1.00x faster                                             |
| xml_etree_parse      | 127 ms                                                                 | 128 ms: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.00x slower                                             |
| python_startup_no_site | 9.62 ms                                                                | 9.64 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml     | 59.1 ms                                                                | 59.7 ms: 1.01x slower                                             |
| mako           | 15.8 ms                                                                | 16.0 ms: 1.01x slower                                             |
| genshi_text    | 28.0 ms                                                                | 28.4 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits                   | 216 ms                                                                 | 206 ms: 1.05x faster                                              |
| logging_silent             | 115 ns                                                                 | 111 ns: 1.04x faster                                              |
| pyflate                    | 511 ms                                                                 | 493 ms: 1.04x faster                                              |
| regex_v8                   | 23.8 ms                                                                | 23.1 ms: 1.03x faster                                             |
| richards                   | 57.1 ms                                                                | 55.7 ms: 1.02x faster                                             |
| nbody                      | 132 ms                                                                 | 129 ms: 1.02x faster                                              |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                              |
| pickle_pure_python         | 365 us                                                                 | 358 us: 1.02x faster                                              |
| coroutines                 | 23.7 ms                                                                | 23.3 ms: 1.02x faster                                             |
| fannkuch                   | 496 ms                                                                 | 487 ms: 1.02x faster                                              |
| generators                 | 32.5 ms                                                                | 31.9 ms: 1.02x faster                                             |
| unpickle_pure_python       | 253 us                                                                 | 249 us: 1.02x faster                                              |
| spectral_norm              | 112 ms                                                                 | 110 ms: 1.01x faster                                              |
| nqueens                    | 98.0 ms                                                                | 96.6 ms: 1.01x faster                                             |
| deepcopy_memo              | 38.5 us                                                                | 38.0 us: 1.01x faster                                             |
| chaos                      | 70.3 ms                                                                | 69.4 ms: 1.01x faster                                             |
| richards_super             | 65.8 ms                                                                | 65.0 ms: 1.01x faster                                             |
| pprint_pformat             | 1.71 sec                                                               | 1.69 sec: 1.01x faster                                            |
| docutils                   | 2.83 sec                                                               | 2.80 sec: 1.01x faster                                            |
| hexiom                     | 7.47 ms                                                                | 7.38 ms: 1.01x faster                                             |
| tomli_loads                | 2.37 sec                                                               | 2.35 sec: 1.01x faster                                            |
| raytrace                   | 330 ms                                                                 | 326 ms: 1.01x faster                                              |
| deepcopy_reduce            | 3.17 us                                                                | 3.14 us: 1.01x faster                                             |
| telco                      | 8.62 ms                                                                | 8.54 ms: 1.01x faster                                             |
| logging_format             | 8.22 us                                                                | 8.14 us: 1.01x faster                                             |
| async_tree_io              | 611 ms                                                                 | 606 ms: 1.01x faster                                              |
| json_dumps                 | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                             |
| logging_simple             | 7.20 us                                                                | 7.14 us: 1.01x faster                                             |
| deepcopy                   | 310 us                                                                 | 308 us: 1.01x faster                                              |
| go                         | 141 ms                                                                 | 140 ms: 1.01x faster                                              |
| sqlalchemy_declarative     | 157 ms                                                                 | 156 ms: 1.00x faster                                              |
| scimark_fft                | 391 ms                                                                 | 390 ms: 1.00x faster                                              |
| xml_etree_process          | 70.5 ms                                                                | 70.2 ms: 1.00x faster                                             |
| json_loads                 | 31.3 us                                                                | 31.2 us: 1.00x faster                                             |
| pprint_safe_repr           | 827 ms                                                                 | 824 ms: 1.00x faster                                              |
| async_generators           | 375 ms                                                                 | 374 ms: 1.00x faster                                              |
| 2to3                       | 305 ms                                                                 | 304 ms: 1.00x faster                                              |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.00x slower                                             |
| python_startup_no_site     | 9.62 ms                                                                | 9.64 ms: 1.00x slower                                             |
| scimark_sparse_mat_mult    | 5.76 ms                                                                | 5.78 ms: 1.00x slower                                             |
| many_optionals             | 1.19 ms                                                                | 1.19 ms: 1.00x slower                                             |
| pycparser                  | 1.19 sec                                                               | 1.19 sec: 1.00x slower                                            |
| thrift                     | 892 us                                                                 | 897 us: 1.00x slower                                              |
| async_tree_cpu_io_mixed    | 588 ms                                                                 | 591 ms: 1.01x slower                                              |
| bench_thread_pool          | 3.32 ms                                                                | 3.34 ms: 1.01x slower                                             |
| coverage                   | 96.1 ms                                                                | 96.7 ms: 1.01x slower                                             |
| sqlglot_optimize           | 61.3 ms                                                                | 61.7 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                 | 559 ms: 1.01x slower                                              |
| crypto_pyaes               | 89.1 ms                                                                | 89.7 ms: 1.01x slower                                             |
| subparsers                 | 25.6 ms                                                                | 25.8 ms: 1.01x slower                                             |
| regex_compile              | 151 ms                                                                 | 153 ms: 1.01x slower                                              |
| xml_etree_parse            | 127 ms                                                                 | 128 ms: 1.01x slower                                              |
| dulwich_log                | 82.3 ms                                                                | 83.1 ms: 1.01x slower                                             |
| genshi_xml                 | 59.1 ms                                                                | 59.7 ms: 1.01x slower                                             |
| sqlglot_transpile          | 1.92 ms                                                                | 1.94 ms: 1.01x slower                                             |
| float                      | 75.6 ms                                                                | 76.6 ms: 1.01x slower                                             |
| mako                       | 15.8 ms                                                                | 16.0 ms: 1.01x slower                                             |
| genshi_text                | 28.0 ms                                                                | 28.4 ms: 1.01x slower                                             |
| html5lib                   | 72.0 ms                                                                | 72.9 ms: 1.01x slower                                             |
| sqlalchemy_imperative      | 24.1 ms                                                                | 24.5 ms: 1.02x slower                                             |
| sympy_sum                  | 185 ms                                                                 | 188 ms: 1.02x slower                                              |
| sympy_expand               | 543 ms                                                                 | 552 ms: 1.02x slower                                              |
| typing_runtime_protocols   | 199 us                                                                 | 203 us: 1.02x slower                                              |
| sympy_str                  | 333 ms                                                                 | 340 ms: 1.02x slower                                              |
| sqlglot_parse              | 1.59 ms                                                                | 1.63 ms: 1.02x slower                                             |
| sympy_integrate            | 24.0 ms                                                                | 24.6 ms: 1.02x slower                                             |
| regex_dna                  | 178 ms                                                                 | 185 ms: 1.04x slower                                              |
| regex_effbot               | 2.77 ms                                                                | 2.87 ms: 1.04x slower                                             |
| deltablue                  | 3.94 ms                                                                | 4.10 ms: 1.04x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (27): async_tree_none_tg, async_tree_none, async_tree_memoization_tg, create_gc_cycles, sqlite_synth, gc_traversal, pathlib, comprehensions, scimark_lu, django_template, xml_etree_generate, sphinx, bench_mp_pool, asyncio_websockets, bpe_tokeniser, meteor_contest, mdp, k_core, sqlglot_normalize, async_tree_io_tg, xml_etree_iterparse, async_tree_memoization, shortest_path, connected_components, json, scimark_monte_carlo, pylint

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 54.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x