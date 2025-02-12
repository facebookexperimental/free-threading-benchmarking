# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: e093464
- commit date: 2025-02-11
- overall geometric mean: 1.013x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 302 ms: 1.01x faster                                                  |
| html5lib       | 72.7 ms                                                                | 71.8 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 355 ms                                                                 | 350 ms: 1.01x faster                                                  |
| async_generators           | 381 ms                                                                 | 377 ms: 1.01x faster                                                  |
| async_tree_none            | 289 ms                                                                 | 287 ms: 1.01x faster                                                  |
| async_tree_io              | 610 ms                                                                 | 605 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 542 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 510 ms: 1.02x slower                                                  |
| coroutines                 | 23.2 ms                                                                | 24.4 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 194 ms: 1.11x faster                                                  |
| float          | 76.2 ms                                                                | 71.7 ms: 1.06x faster                                                 |
| nbody          | 130 ms                                                                 | 123 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 171 ms: 1.10x faster                                                  |
| regex_v8       | 24.4 ms                                                                | 23.3 ms: 1.05x faster                                                 |
| regex_effbot   | 2.84 ms                                                                | 2.78 ms: 1.02x faster                                                 |
| regex_compile  | 152 ms                                                                 | 151 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                                               | 2.27 sec: 1.03x faster                                                |
| unpickle_pure_python | 248 us                                                                 | 243 us: 1.02x faster                                                  |
| pickle_pure_python   | 368 us                                                                 | 364 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 88.1 ms                                                                | 88.5 ms: 1.01x slower                                                 |
| xml_etree_process    | 68.8 ms                                                                | 69.5 ms: 1.01x slower                                                 |
| json_loads           | 31.1 us                                                                | 31.5 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_generate, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 15.7 ms: 1.01x faster                                                 |
| django_template | 42.2 ms                                                                | 42.4 ms: 1.01x slower                                                 |
| genshi_xml      | 58.7 ms                                                                | 59.1 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 216 ms                                                                 | 194 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 5.67 ms                                                                | 5.14 ms: 1.10x faster                                                 |
| regex_dna                  | 187 ms                                                                 | 171 ms: 1.10x faster                                                  |
| scimark_fft                | 387 ms                                                                 | 359 ms: 1.08x faster                                                  |
| gc_traversal               | 1.76 ms                                                                | 1.65 ms: 1.06x faster                                                 |
| float                      | 76.2 ms                                                                | 71.7 ms: 1.06x faster                                                 |
| nbody                      | 130 ms                                                                 | 123 ms: 1.06x faster                                                  |
| fannkuch                   | 493 ms                                                                 | 468 ms: 1.05x faster                                                  |
| raytrace                   | 330 ms                                                                 | 314 ms: 1.05x faster                                                  |
| regex_v8                   | 24.4 ms                                                                | 23.3 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 82.4 ms                                                                | 78.7 ms: 1.05x faster                                                 |
| meteor_contest             | 132 ms                                                                 | 126 ms: 1.04x faster                                                  |
| scimark_lu                 | 140 ms                                                                 | 134 ms: 1.04x faster                                                  |
| chaos                      | 71.1 ms                                                                | 68.8 ms: 1.03x faster                                                 |
| scimark_sor                | 135 ms                                                                 | 130 ms: 1.03x faster                                                  |
| connected_components       | 497 ms                                                                 | 482 ms: 1.03x faster                                                  |
| tomli_loads                | 2.33 sec                                                               | 2.27 sec: 1.03x faster                                                |
| logging_silent             | 113 ns                                                                 | 110 ns: 1.03x faster                                                  |
| sqlglot_parse              | 1.58 ms                                                                | 1.54 ms: 1.03x faster                                                 |
| sqlglot_transpile          | 1.91 ms                                                                | 1.86 ms: 1.03x faster                                                 |
| many_optionals             | 1.18 ms                                                                | 1.15 ms: 1.03x faster                                                 |
| deepcopy_memo              | 37.9 us                                                                | 36.9 us: 1.03x faster                                                 |
| logging_format             | 8.42 us                                                                | 8.21 us: 1.02x faster                                                 |
| sqlite_synth               | 2.06 us                                                                | 2.01 us: 1.02x faster                                                 |
| deltablue                  | 4.70 ms                                                                | 4.60 ms: 1.02x faster                                                 |
| regex_effbot               | 2.84 ms                                                                | 2.78 ms: 1.02x faster                                                 |
| richards                   | 56.5 ms                                                                | 55.4 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 248 us                                                                 | 243 us: 1.02x faster                                                  |
| pyflate                    | 492 ms                                                                 | 483 ms: 1.02x faster                                                  |
| shortest_path              | 547 ms                                                                 | 539 ms: 1.02x faster                                                  |
| go                         | 138 ms                                                                 | 136 ms: 1.01x faster                                                  |
| richards_super             | 65.3 ms                                                                | 64.4 ms: 1.01x faster                                                 |
| deepcopy                   | 309 us                                                                 | 304 us: 1.01x faster                                                  |
| async_tree_memoization     | 355 ms                                                                 | 350 ms: 1.01x faster                                                  |
| telco                      | 8.49 ms                                                                | 8.38 ms: 1.01x faster                                                 |
| pickle_pure_python         | 368 us                                                                 | 364 us: 1.01x faster                                                  |
| html5lib                   | 72.7 ms                                                                | 71.8 ms: 1.01x faster                                                 |
| mako                       | 15.9 ms                                                                | 15.7 ms: 1.01x faster                                                 |
| crypto_pyaes               | 88.9 ms                                                                | 87.8 ms: 1.01x faster                                                 |
| nqueens                    | 97.4 ms                                                                | 96.3 ms: 1.01x faster                                                 |
| sqlglot_optimize           | 61.3 ms                                                                | 60.7 ms: 1.01x faster                                                 |
| hexiom                     | 7.48 ms                                                                | 7.40 ms: 1.01x faster                                                 |
| sympy_str                  | 337 ms                                                                 | 334 ms: 1.01x faster                                                  |
| async_generators           | 381 ms                                                                 | 377 ms: 1.01x faster                                                  |
| logging_simple             | 7.36 us                                                                | 7.29 us: 1.01x faster                                                 |
| thrift                     | 908 us                                                                 | 900 us: 1.01x faster                                                  |
| regex_compile              | 152 ms                                                                 | 151 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 120 ms                                                                 | 119 ms: 1.01x faster                                                  |
| 2to3                       | 305 ms                                                                 | 302 ms: 1.01x faster                                                  |
| async_tree_none            | 289 ms                                                                 | 287 ms: 1.01x faster                                                  |
| async_tree_io              | 610 ms                                                                 | 605 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                                 | 109 ms: 1.01x faster                                                  |
| k_core                     | 2.31 sec                                                               | 2.29 sec: 1.01x faster                                                |
| create_gc_cycles           | 1.39 ms                                                                | 1.38 ms: 1.01x faster                                                 |
| comprehensions             | 19.9 us                                                                | 19.8 us: 1.01x faster                                                 |
| sympy_expand               | 549 ms                                                                 | 546 ms: 1.01x faster                                                  |
| sympy_integrate            | 24.0 ms                                                                | 23.9 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.30 ms                                                                | 3.29 ms: 1.00x faster                                                 |
| json                       | 5.37 ms                                                                | 5.39 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 801 ms                                                                 | 806 ms: 1.01x slower                                                  |
| xml_etree_iterparse        | 88.1 ms                                                                | 88.5 ms: 1.01x slower                                                 |
| django_template            | 42.2 ms                                                                | 42.4 ms: 1.01x slower                                                 |
| genshi_xml                 | 58.7 ms                                                                | 59.1 ms: 1.01x slower                                                 |
| mdp                        | 2.69 sec                                                               | 2.71 sec: 1.01x slower                                                |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.01x slower                                                  |
| pycparser                  | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                                |
| dulwich_log                | 81.9 ms                                                                | 82.5 ms: 1.01x slower                                                 |
| xml_etree_process          | 68.8 ms                                                                | 69.5 ms: 1.01x slower                                                 |
| json_loads                 | 31.1 us                                                                | 31.5 us: 1.01x slower                                                 |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 542 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 510 ms: 1.02x slower                                                  |
| coverage                   | 96.5 ms                                                                | 98.9 ms: 1.02x slower                                                 |
| coroutines                 | 23.2 ms                                                                | 24.4 ms: 1.06x slower                                                 |
| generators                 | 32.1 ms                                                                | 34.8 ms: 1.08x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (22): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, bench_mp_pool, asyncio_websockets, deepcopy_reduce, genshi_text, sphinx, xml_etree_parse, subparsers, docutils, bpe_tokeniser, sympy_sum, python_startup_no_site, python_startup, pathlib, xml_etree_generate, pprint_pformat, json_dumps, sqlalchemy_imperative, typing_runtime_protocols, pylint

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x