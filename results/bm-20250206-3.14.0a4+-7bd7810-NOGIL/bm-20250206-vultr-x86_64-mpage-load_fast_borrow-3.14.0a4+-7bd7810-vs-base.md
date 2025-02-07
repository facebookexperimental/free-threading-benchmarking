# Results vs. base

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: 7bd7810
- commit date: 2025-02-06
- overall geometric mean: 1.008x faster
- HPT reliability: 99.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| html5lib       | 72.7 ms                                                                | 70.4 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 250 ms                                                                 | 242 ms: 1.03x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 345 ms: 1.03x faster                                              |
| async_tree_memoization_tg  | 320 ms                                                                 | 313 ms: 1.02x faster                                              |
| async_tree_io_tg           | 576 ms                                                                 | 563 ms: 1.02x faster                                              |
| async_tree_none            | 289 ms                                                                 | 284 ms: 1.02x faster                                              |
| async_generators           | 381 ms                                                                 | 375 ms: 1.02x faster                                              |
| async_tree_io              | 610 ms                                                                 | 602 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 495 ms: 1.01x faster                                              |
| coroutines                 | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| float          | 76.2 ms                                                                | 72.6 ms: 1.05x faster                                             |
| nbody          | 130 ms                                                                 | 132 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 185 ms: 1.01x faster                                              |
| regex_compile  | 152 ms                                                                 | 151 ms: 1.01x faster                                              |
| regex_effbot   | 2.84 ms                                                                | 2.94 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 368 us                                                                 | 355 us: 1.04x faster                                              |
| unpickle_pure_python | 248 us                                                                 | 243 us: 1.02x faster                                              |
| xml_etree_process    | 68.8 ms                                                                | 68.1 ms: 1.01x faster                                             |
| xml_etree_generate   | 96.6 ms                                                                | 95.8 ms: 1.01x faster                                             |
| tomli_loads          | 2.33 sec                                                               | 2.34 sec: 1.00x slower                                            |
| json_loads           | 31.1 us                                                                | 31.6 us: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (3): json_dumps, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.63 ms                                                                | 9.78 ms: 1.02x slower                                             |
| python_startup         | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 42.2 ms                                                                | 41.5 ms: 1.02x faster                                             |
| mako            | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                             |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| scimark_sor                | 135 ms                                                                 | 128 ms: 1.05x faster                                              |
| float                      | 76.2 ms                                                                | 72.6 ms: 1.05x faster                                             |
| gc_traversal               | 1.76 ms                                                                | 1.68 ms: 1.04x faster                                             |
| chaos                      | 71.1 ms                                                                | 68.4 ms: 1.04x faster                                             |
| raytrace                   | 330 ms                                                                 | 318 ms: 1.04x faster                                              |
| pickle_pure_python         | 368 us                                                                 | 355 us: 1.04x faster                                              |
| sqlglot_parse              | 1.58 ms                                                                | 1.53 ms: 1.04x faster                                             |
| logging_format             | 8.42 us                                                                | 8.14 us: 1.03x faster                                             |
| html5lib                   | 72.7 ms                                                                | 70.4 ms: 1.03x faster                                             |
| meteor_contest             | 132 ms                                                                 | 128 ms: 1.03x faster                                              |
| sqlglot_transpile          | 1.91 ms                                                                | 1.85 ms: 1.03x faster                                             |
| async_tree_none_tg         | 250 ms                                                                 | 242 ms: 1.03x faster                                              |
| logging_silent             | 113 ns                                                                 | 110 ns: 1.03x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 345 ms: 1.03x faster                                              |
| nqueens                    | 97.4 ms                                                                | 95.2 ms: 1.02x faster                                             |
| async_tree_memoization_tg  | 320 ms                                                                 | 313 ms: 1.02x faster                                              |
| async_tree_io_tg           | 576 ms                                                                 | 563 ms: 1.02x faster                                              |
| sqlglot_normalize          | 120 ms                                                                 | 117 ms: 1.02x faster                                              |
| unpickle_pure_python       | 248 us                                                                 | 243 us: 1.02x faster                                              |
| scimark_lu                 | 140 ms                                                                 | 137 ms: 1.02x faster                                              |
| logging_simple             | 7.36 us                                                                | 7.22 us: 1.02x faster                                             |
| django_template            | 42.2 ms                                                                | 41.5 ms: 1.02x faster                                             |
| deltablue                  | 4.70 ms                                                                | 4.62 ms: 1.02x faster                                             |
| async_tree_none            | 289 ms                                                                 | 284 ms: 1.02x faster                                              |
| async_generators           | 381 ms                                                                 | 375 ms: 1.02x faster                                              |
| richards                   | 56.5 ms                                                                | 55.6 ms: 1.02x faster                                             |
| coverage                   | 96.5 ms                                                                | 95.1 ms: 1.02x faster                                             |
| sqlglot_optimize           | 61.3 ms                                                                | 60.4 ms: 1.01x faster                                             |
| regex_dna                  | 187 ms                                                                 | 185 ms: 1.01x faster                                              |
| crypto_pyaes               | 88.9 ms                                                                | 87.7 ms: 1.01x faster                                             |
| async_tree_io              | 610 ms                                                                 | 602 ms: 1.01x faster                                              |
| connected_components       | 497 ms                                                                 | 491 ms: 1.01x faster                                              |
| deepcopy                   | 309 us                                                                 | 305 us: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 495 ms: 1.01x faster                                              |
| xml_etree_process          | 68.8 ms                                                                | 68.1 ms: 1.01x faster                                             |
| xml_etree_generate         | 96.6 ms                                                                | 95.8 ms: 1.01x faster                                             |
| deepcopy_memo              | 37.9 us                                                                | 37.6 us: 1.01x faster                                             |
| scimark_monte_carlo        | 82.4 ms                                                                | 81.8 ms: 1.01x faster                                             |
| fannkuch                   | 493 ms                                                                 | 490 ms: 1.01x faster                                              |
| generators                 | 32.1 ms                                                                | 31.9 ms: 1.01x faster                                             |
| regex_compile              | 152 ms                                                                 | 151 ms: 1.01x faster                                              |
| go                         | 138 ms                                                                 | 138 ms: 1.01x faster                                              |
| sympy_str                  | 337 ms                                                                 | 336 ms: 1.00x faster                                              |
| bpe_tokeniser              | 4.68 sec                                                               | 4.66 sec: 1.00x faster                                            |
| mako                       | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                             |
| pprint_safe_repr           | 801 ms                                                                 | 803 ms: 1.00x slower                                              |
| k_core                     | 2.31 sec                                                               | 2.31 sec: 1.00x slower                                            |
| hexiom                     | 7.48 ms                                                                | 7.50 ms: 1.00x slower                                             |
| coroutines                 | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                             |
| tomli_loads                | 2.33 sec                                                               | 2.34 sec: 1.00x slower                                            |
| pycparser                  | 1.18 sec                                                               | 1.19 sec: 1.00x slower                                            |
| pyflate                    | 492 ms                                                                 | 494 ms: 1.01x slower                                              |
| sympy_integrate            | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                             |
| mdp                        | 2.69 sec                                                               | 2.71 sec: 1.01x slower                                            |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.01x slower                                              |
| spectral_norm              | 110 ms                                                                 | 111 ms: 1.01x slower                                              |
| scimark_fft                | 387 ms                                                                 | 392 ms: 1.01x slower                                              |
| many_optionals             | 1.18 ms                                                                | 1.19 ms: 1.01x slower                                             |
| nbody                      | 130 ms                                                                 | 132 ms: 1.01x slower                                              |
| pathlib                    | 18.6 ms                                                                | 18.8 ms: 1.01x slower                                             |
| json_loads                 | 31.1 us                                                                | 31.6 us: 1.02x slower                                             |
| create_gc_cycles           | 1.39 ms                                                                | 1.41 ms: 1.02x slower                                             |
| python_startup_no_site     | 9.63 ms                                                                | 9.78 ms: 1.02x slower                                             |
| json                       | 5.37 ms                                                                | 5.46 ms: 1.02x slower                                             |
| python_startup             | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                             |
| dulwich_log                | 81.9 ms                                                                | 83.4 ms: 1.02x slower                                             |
| subparsers                 | 25.3 ms                                                                | 25.8 ms: 1.02x slower                                             |
| bench_mp_pool              | 93.4 ms                                                                | 95.5 ms: 1.02x slower                                             |
| telco                      | 8.49 ms                                                                | 8.71 ms: 1.03x slower                                             |
| scimark_sparse_mat_mult    | 5.67 ms                                                                | 5.83 ms: 1.03x slower                                             |
| regex_effbot               | 2.84 ms                                                                | 2.94 ms: 1.03x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (24): thrift, shortest_path, richards_super, async_tree_cpu_io_mixed, genshi_xml, json_dumps, typing_runtime_protocols, xml_etree_iterparse, deepcopy_reduce, pprint_pformat, sqlite_synth, genshi_text, asyncio_websockets, sphinx, 2to3, docutils, sympy_expand, bench_thread_pool, comprehensions, sympy_sum, xml_etree_parse, sqlalchemy_imperative, regex_v8, pylint

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 99.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x