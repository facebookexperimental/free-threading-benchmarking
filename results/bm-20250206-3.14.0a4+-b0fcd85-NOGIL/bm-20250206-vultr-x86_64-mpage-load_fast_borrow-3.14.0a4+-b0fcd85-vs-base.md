# Results vs. base

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: b0fcd85
- commit date: 2025-02-06
- overall geometric mean: 1.012x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 303 ms: 1.00x faster                                              |
| html5lib       | 72.7 ms                                                                | 72.3 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 250 ms                                                                 | 241 ms: 1.04x faster                                              |
| async_tree_io_tg           | 576 ms                                                                 | 556 ms: 1.04x faster                                              |
| async_tree_io              | 610 ms                                                                 | 589 ms: 1.03x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 344 ms: 1.03x faster                                              |
| async_tree_none            | 289 ms                                                                 | 281 ms: 1.03x faster                                              |
| async_tree_memoization_tg  | 320 ms                                                                 | 312 ms: 1.03x faster                                              |
| async_generators           | 381 ms                                                                 | 372 ms: 1.03x faster                                              |
| coroutines                 | 23.2 ms                                                                | 22.9 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 531 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 497 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 202 ms: 1.07x faster                                              |
| float          | 76.2 ms                                                                | 73.0 ms: 1.04x faster                                             |
| nbody          | 130 ms                                                                 | 131 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 23.2 ms: 1.05x faster                                             |
| regex_dna      | 187 ms                                                                 | 184 ms: 1.02x faster                                              |
| regex_effbot   | 2.84 ms                                                                | 2.79 ms: 1.02x faster                                             |
| regex_compile  | 152 ms                                                                 | 152 ms: 1.00x faster                                              |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 368 us                                                                 | 354 us: 1.04x faster                                              |
| unpickle_pure_python | 248 us                                                                 | 240 us: 1.03x faster                                              |
| xml_etree_generate   | 96.6 ms                                                                | 95.2 ms: 1.01x faster                                             |
| xml_etree_process    | 68.8 ms                                                                | 68.0 ms: 1.01x faster                                             |
| xml_etree_iterparse  | 88.1 ms                                                                | 87.3 ms: 1.01x faster                                             |
| json_dumps           | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                             |
| json_loads           | 31.1 us                                                                | 31.6 us: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.63 ms                                                                | 9.77 ms: 1.02x slower                                             |
| python_startup         | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 42.2 ms                                                                | 41.4 ms: 1.02x faster                                             |
| mako            | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits                   | 216 ms                                                                 | 202 ms: 1.07x faster                                              |
| raytrace                   | 330 ms                                                                 | 310 ms: 1.07x faster                                              |
| chaos                      | 71.1 ms                                                                | 67.1 ms: 1.06x faster                                             |
| logging_silent             | 113 ns                                                                 | 106 ns: 1.06x faster                                              |
| regex_v8                   | 24.4 ms                                                                | 23.2 ms: 1.05x faster                                             |
| gc_traversal               | 1.76 ms                                                                | 1.67 ms: 1.05x faster                                             |
| scimark_sor                | 135 ms                                                                 | 129 ms: 1.05x faster                                              |
| float                      | 76.2 ms                                                                | 73.0 ms: 1.04x faster                                             |
| sqlglot_parse              | 1.58 ms                                                                | 1.52 ms: 1.04x faster                                             |
| pickle_pure_python         | 368 us                                                                 | 354 us: 1.04x faster                                              |
| async_tree_none_tg         | 250 ms                                                                 | 241 ms: 1.04x faster                                              |
| sqlglot_transpile          | 1.91 ms                                                                | 1.84 ms: 1.04x faster                                             |
| async_tree_io_tg           | 576 ms                                                                 | 556 ms: 1.04x faster                                              |
| async_tree_io              | 610 ms                                                                 | 589 ms: 1.03x faster                                              |
| unpickle_pure_python       | 248 us                                                                 | 240 us: 1.03x faster                                              |
| deltablue                  | 4.70 ms                                                                | 4.55 ms: 1.03x faster                                             |
| async_tree_memoization     | 355 ms                                                                 | 344 ms: 1.03x faster                                              |
| logging_simple             | 7.36 us                                                                | 7.14 us: 1.03x faster                                             |
| scimark_lu                 | 140 ms                                                                 | 136 ms: 1.03x faster                                              |
| async_tree_none            | 289 ms                                                                 | 281 ms: 1.03x faster                                              |
| thrift                     | 908 us                                                                 | 883 us: 1.03x faster                                              |
| async_tree_memoization_tg  | 320 ms                                                                 | 312 ms: 1.03x faster                                              |
| async_generators           | 381 ms                                                                 | 372 ms: 1.03x faster                                              |
| sqlglot_normalize          | 120 ms                                                                 | 117 ms: 1.02x faster                                              |
| logging_format             | 8.42 us                                                                | 8.22 us: 1.02x faster                                             |
| comprehensions             | 19.9 us                                                                | 19.5 us: 1.02x faster                                             |
| deepcopy_reduce            | 3.19 us                                                                | 3.12 us: 1.02x faster                                             |
| sqlite_synth               | 2.06 us                                                                | 2.01 us: 1.02x faster                                             |
| deepcopy_memo              | 37.9 us                                                                | 37.1 us: 1.02x faster                                             |
| regex_dna                  | 187 ms                                                                 | 184 ms: 1.02x faster                                              |
| meteor_contest             | 132 ms                                                                 | 129 ms: 1.02x faster                                              |
| regex_effbot               | 2.84 ms                                                                | 2.79 ms: 1.02x faster                                             |
| django_template            | 42.2 ms                                                                | 41.4 ms: 1.02x faster                                             |
| hexiom                     | 7.48 ms                                                                | 7.36 ms: 1.02x faster                                             |
| richards                   | 56.5 ms                                                                | 55.6 ms: 1.02x faster                                             |
| scimark_monte_carlo        | 82.4 ms                                                                | 81.2 ms: 1.02x faster                                             |
| pyflate                    | 492 ms                                                                 | 485 ms: 1.01x faster                                              |
| sqlglot_optimize           | 61.3 ms                                                                | 60.4 ms: 1.01x faster                                             |
| xml_etree_generate         | 96.6 ms                                                                | 95.2 ms: 1.01x faster                                             |
| deepcopy                   | 309 us                                                                 | 304 us: 1.01x faster                                              |
| nqueens                    | 97.4 ms                                                                | 96.2 ms: 1.01x faster                                             |
| go                         | 138 ms                                                                 | 137 ms: 1.01x faster                                              |
| xml_etree_process          | 68.8 ms                                                                | 68.0 ms: 1.01x faster                                             |
| coroutines                 | 23.2 ms                                                                | 22.9 ms: 1.01x faster                                             |
| fannkuch                   | 493 ms                                                                 | 489 ms: 1.01x faster                                              |
| xml_etree_iterparse        | 88.1 ms                                                                | 87.3 ms: 1.01x faster                                             |
| crypto_pyaes               | 88.9 ms                                                                | 88.1 ms: 1.01x faster                                             |
| pprint_safe_repr           | 801 ms                                                                 | 795 ms: 1.01x faster                                              |
| scimark_fft                | 387 ms                                                                 | 385 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 531 ms: 1.01x faster                                              |
| pprint_pformat             | 1.66 sec                                                               | 1.65 sec: 1.01x faster                                            |
| bpe_tokeniser              | 4.68 sec                                                               | 4.65 sec: 1.01x faster                                            |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 497 ms: 1.01x faster                                              |
| json_dumps                 | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                             |
| html5lib                   | 72.7 ms                                                                | 72.3 ms: 1.01x faster                                             |
| 2to3                       | 305 ms                                                                 | 303 ms: 1.00x faster                                              |
| regex_compile              | 152 ms                                                                 | 152 ms: 1.00x faster                                              |
| sympy_integrate            | 24.0 ms                                                                | 24.1 ms: 1.00x slower                                             |
| mako                       | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                             |
| spectral_norm              | 110 ms                                                                 | 110 ms: 1.00x slower                                              |
| coverage                   | 96.5 ms                                                                | 97.2 ms: 1.01x slower                                             |
| json                       | 5.37 ms                                                                | 5.41 ms: 1.01x slower                                             |
| create_gc_cycles           | 1.39 ms                                                                | 1.40 ms: 1.01x slower                                             |
| subparsers                 | 25.3 ms                                                                | 25.5 ms: 1.01x slower                                             |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.01x slower                                              |
| dulwich_log                | 81.9 ms                                                                | 82.7 ms: 1.01x slower                                             |
| nbody                      | 130 ms                                                                 | 131 ms: 1.01x slower                                              |
| sympy_expand               | 549 ms                                                                 | 555 ms: 1.01x slower                                              |
| sympy_sum                  | 186 ms                                                                 | 188 ms: 1.01x slower                                              |
| python_startup_no_site     | 9.63 ms                                                                | 9.77 ms: 1.02x slower                                             |
| json_loads                 | 31.1 us                                                                | 31.6 us: 1.02x slower                                             |
| telco                      | 8.49 ms                                                                | 8.64 ms: 1.02x slower                                             |
| python_startup             | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                             |
| bench_mp_pool              | 93.4 ms                                                                | 95.9 ms: 1.03x slower                                             |
| scimark_sparse_mat_mult    | 5.67 ms                                                                | 5.83 ms: 1.03x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (21): connected_components, richards_super, xml_etree_parse, genshi_text, bench_thread_pool, pycparser, mdp, sphinx, docutils, tomli_loads, generators, asyncio_websockets, k_core, sympy_str, genshi_xml, pathlib, many_optionals, shortest_path, typing_runtime_protocols, pylint, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x