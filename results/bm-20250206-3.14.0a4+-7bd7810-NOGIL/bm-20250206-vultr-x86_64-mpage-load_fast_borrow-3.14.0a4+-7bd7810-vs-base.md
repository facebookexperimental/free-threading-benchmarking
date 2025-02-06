# Results vs. base

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: 7bd7810
- commit date: 2025-02-06
- overall geometric mean: 1.011x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 304 ms: 1.00x faster                                              |
| html5lib       | 72.7 ms                                                                | 72.2 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 250 ms                                                                 | 241 ms: 1.04x faster                                              |
| async_tree_memoization_tg  | 320 ms                                                                 | 310 ms: 1.03x faster                                              |
| async_tree_none            | 289 ms                                                                 | 281 ms: 1.03x faster                                              |
| async_tree_io              | 610 ms                                                                 | 592 ms: 1.03x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 345 ms: 1.03x faster                                              |
| async_tree_io_tg           | 576 ms                                                                 | 560 ms: 1.03x faster                                              |
| async_generators           | 381 ms                                                                 | 373 ms: 1.02x faster                                              |
| coroutines                 | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                             |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 531 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 498 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 76.2 ms                                                                | 72.5 ms: 1.05x faster                                             |
| pidigits       | 216 ms                                                                 | 207 ms: 1.04x faster                                              |
| nbody          | 130 ms                                                                 | 131 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 23.3 ms: 1.05x faster                                             |
| regex_dna      | 187 ms                                                                 | 180 ms: 1.04x faster                                              |
| regex_effbot   | 2.84 ms                                                                | 2.75 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 368 us                                                                 | 357 us: 1.03x faster                                              |
| unpickle_pure_python | 248 us                                                                 | 243 us: 1.02x faster                                              |
| xml_etree_process    | 68.8 ms                                                                | 67.7 ms: 1.02x faster                                             |
| xml_etree_generate   | 96.6 ms                                                                | 95.7 ms: 1.01x faster                                             |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                              |
| tomli_loads          | 2.33 sec                                                               | 2.34 sec: 1.00x slower                                            |
| json_loads           | 31.1 us                                                                | 31.2 us: 1.00x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.63 ms                                                                | 9.79 ms: 1.02x slower                                             |
| python_startup         | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 15.7 ms: 1.01x faster                                             |
| django_template | 42.2 ms                                                                | 41.7 ms: 1.01x faster                                             |
| genshi_xml      | 58.7 ms                                                                | 59.4 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| logging_silent             | 113 ns                                                                 | 106 ns: 1.06x faster                                              |
| gc_traversal               | 1.76 ms                                                                | 1.66 ms: 1.06x faster                                             |
| chaos                      | 71.1 ms                                                                | 67.6 ms: 1.05x faster                                             |
| float                      | 76.2 ms                                                                | 72.5 ms: 1.05x faster                                             |
| scimark_sor                | 135 ms                                                                 | 128 ms: 1.05x faster                                              |
| regex_v8                   | 24.4 ms                                                                | 23.3 ms: 1.05x faster                                             |
| raytrace                   | 330 ms                                                                 | 316 ms: 1.05x faster                                              |
| pidigits                   | 216 ms                                                                 | 207 ms: 1.04x faster                                              |
| regex_dna                  | 187 ms                                                                 | 180 ms: 1.04x faster                                              |
| scimark_lu                 | 140 ms                                                                 | 135 ms: 1.04x faster                                              |
| async_tree_none_tg         | 250 ms                                                                 | 241 ms: 1.04x faster                                              |
| regex_effbot               | 2.84 ms                                                                | 2.75 ms: 1.03x faster                                             |
| pickle_pure_python         | 368 us                                                                 | 357 us: 1.03x faster                                              |
| sqlglot_parse              | 1.58 ms                                                                | 1.53 ms: 1.03x faster                                             |
| async_tree_memoization_tg  | 320 ms                                                                 | 310 ms: 1.03x faster                                              |
| async_tree_none            | 289 ms                                                                 | 281 ms: 1.03x faster                                              |
| async_tree_io              | 610 ms                                                                 | 592 ms: 1.03x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 345 ms: 1.03x faster                                              |
| async_tree_io_tg           | 576 ms                                                                 | 560 ms: 1.03x faster                                              |
| sqlglot_transpile          | 1.91 ms                                                                | 1.86 ms: 1.03x faster                                             |
| deltablue                  | 4.70 ms                                                                | 4.59 ms: 1.02x faster                                             |
| sqlite_synth               | 2.06 us                                                                | 2.01 us: 1.02x faster                                             |
| meteor_contest             | 132 ms                                                                 | 129 ms: 1.02x faster                                              |
| richards                   | 56.5 ms                                                                | 55.3 ms: 1.02x faster                                             |
| async_generators           | 381 ms                                                                 | 373 ms: 1.02x faster                                              |
| unpickle_pure_python       | 248 us                                                                 | 243 us: 1.02x faster                                              |
| coroutines                 | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                             |
| coverage                   | 96.5 ms                                                                | 94.7 ms: 1.02x faster                                             |
| nqueens                    | 97.4 ms                                                                | 95.6 ms: 1.02x faster                                             |
| hexiom                     | 7.48 ms                                                                | 7.34 ms: 1.02x faster                                             |
| sqlglot_normalize          | 120 ms                                                                 | 118 ms: 1.02x faster                                              |
| pyflate                    | 492 ms                                                                 | 483 ms: 1.02x faster                                              |
| thrift                     | 908 us                                                                 | 893 us: 1.02x faster                                              |
| deepcopy_memo              | 37.9 us                                                                | 37.3 us: 1.02x faster                                             |
| xml_etree_process          | 68.8 ms                                                                | 67.7 ms: 1.02x faster                                             |
| mako                       | 15.9 ms                                                                | 15.7 ms: 1.01x faster                                             |
| django_template            | 42.2 ms                                                                | 41.7 ms: 1.01x faster                                             |
| richards_super             | 65.3 ms                                                                | 64.5 ms: 1.01x faster                                             |
| generators                 | 32.1 ms                                                                | 31.7 ms: 1.01x faster                                             |
| logging_format             | 8.42 us                                                                | 8.32 us: 1.01x faster                                             |
| crypto_pyaes               | 88.9 ms                                                                | 87.9 ms: 1.01x faster                                             |
| deepcopy_reduce            | 3.19 us                                                                | 3.15 us: 1.01x faster                                             |
| go                         | 138 ms                                                                 | 137 ms: 1.01x faster                                              |
| deepcopy                   | 309 us                                                                 | 305 us: 1.01x faster                                              |
| sqlglot_optimize           | 61.3 ms                                                                | 60.7 ms: 1.01x faster                                             |
| typing_runtime_protocols   | 198 us                                                                 | 196 us: 1.01x faster                                              |
| xml_etree_generate         | 96.6 ms                                                                | 95.7 ms: 1.01x faster                                             |
| connected_components       | 497 ms                                                                 | 493 ms: 1.01x faster                                              |
| fannkuch                   | 493 ms                                                                 | 489 ms: 1.01x faster                                              |
| comprehensions             | 19.9 us                                                                | 19.8 us: 1.01x faster                                             |
| html5lib                   | 72.7 ms                                                                | 72.2 ms: 1.01x faster                                             |
| bench_thread_pool          | 3.30 ms                                                                | 3.28 ms: 1.01x faster                                             |
| xml_etree_parse            | 128 ms                                                                 | 127 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.68 sec                                                               | 4.65 sec: 1.01x faster                                            |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 531 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 498 ms: 1.00x faster                                              |
| mdp                        | 2.69 sec                                                               | 2.68 sec: 1.00x faster                                            |
| scimark_fft                | 387 ms                                                                 | 387 ms: 1.00x faster                                              |
| 2to3                       | 305 ms                                                                 | 304 ms: 1.00x faster                                              |
| spectral_norm              | 110 ms                                                                 | 110 ms: 1.00x slower                                              |
| scimark_monte_carlo        | 82.4 ms                                                                | 82.7 ms: 1.00x slower                                             |
| many_optionals             | 1.18 ms                                                                | 1.18 ms: 1.00x slower                                             |
| tomli_loads                | 2.33 sec                                                               | 2.34 sec: 1.00x slower                                            |
| json_loads                 | 31.1 us                                                                | 31.2 us: 1.00x slower                                             |
| sympy_sum                  | 186 ms                                                                 | 187 ms: 1.00x slower                                              |
| k_core                     | 2.31 sec                                                               | 2.32 sec: 1.00x slower                                            |
| sympy_integrate            | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                             |
| telco                      | 8.49 ms                                                                | 8.57 ms: 1.01x slower                                             |
| sqlalchemy_declarative     | 157 ms                                                                 | 159 ms: 1.01x slower                                              |
| nbody                      | 130 ms                                                                 | 131 ms: 1.01x slower                                              |
| scimark_sparse_mat_mult    | 5.67 ms                                                                | 5.73 ms: 1.01x slower                                             |
| genshi_xml                 | 58.7 ms                                                                | 59.4 ms: 1.01x slower                                             |
| sqlalchemy_imperative      | 24.4 ms                                                                | 24.8 ms: 1.02x slower                                             |
| python_startup_no_site     | 9.63 ms                                                                | 9.79 ms: 1.02x slower                                             |
| dulwich_log                | 81.9 ms                                                                | 83.3 ms: 1.02x slower                                             |
| pycparser                  | 1.18 sec                                                               | 1.20 sec: 1.02x slower                                            |
| python_startup             | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                             |
| bench_mp_pool              | 93.4 ms                                                                | 95.5 ms: 1.02x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (18): logging_simple, json, create_gc_cycles, pprint_pformat, sphinx, xml_etree_iterparse, regex_compile, sympy_str, pprint_safe_repr, shortest_path, asyncio_websockets, pathlib, docutils, genshi_text, json_dumps, sympy_expand, subparsers, pylint

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x