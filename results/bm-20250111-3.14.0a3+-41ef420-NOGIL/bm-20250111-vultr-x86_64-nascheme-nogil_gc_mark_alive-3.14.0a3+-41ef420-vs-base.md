# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.009x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 345 ms                                                                 | 339 ms: 1.02x faster                                                    |
| sphinx         | 1.16 sec                                                               | 1.14 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                 | 23.1 ms                                                                | 22.8 ms: 1.02x faster                                                   |
| async_tree_memoization     | 431 ms                                                                 | 427 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 598 ms                                                                 | 601 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                 | 574 ms: 1.02x slower                                                    |
| async_generators           | 430 ms                                                                 | 447 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_io_tg, asyncio_websockets, async_tree_none, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 182 ms: 1.08x faster                                                    |
| nbody          | 129 ms                                                                 | 126 ms: 1.02x faster                                                    |
| float          | 106 ms                                                                 | 105 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 173 ms: 1.05x faster                                                    |
| regex_v8       | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                                   |
| regex_effbot   | 2.69 ms                                                                | 2.74 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 14.1 ms                                                                | 13.8 ms: 1.02x faster                                                   |
| xml_etree_iterparse | 90.0 ms                                                                | 88.4 ms: 1.02x faster                                                   |
| xml_etree_parse     | 130 ms                                                                 | 128 ms: 1.01x faster                                                    |
| pickle_pure_python  | 493 us                                                                 | 489 us: 1.01x faster                                                    |
| xml_etree_process   | 73.3 ms                                                                | 73.0 ms: 1.00x faster                                                   |
| xml_etree_generate  | 97.3 ms                                                                | 96.9 ms: 1.00x faster                                                   |
| tomli_loads         | 2.32 sec                                                               | 2.34 sec: 1.01x slower                                                  |
| json_loads          | 28.6 us                                                                | 29.3 us: 1.02x slower                                                   |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.6 ms: 1.01x faster                                                   |
| python_startup_no_site | 9.82 ms                                                                | 9.76 ms: 1.01x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 62.7 ms                                                                | 62.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (3): django_template, mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles           | 1.84 ms                                                                | 1.45 ms: 1.27x faster                                                   |
| pidigits                   | 197 ms                                                                 | 182 ms: 1.08x faster                                                    |
| bench_mp_pool              | 100 ms                                                                 | 93.8 ms: 1.07x faster                                                   |
| regex_dna                  | 181 ms                                                                 | 173 ms: 1.05x faster                                                    |
| gc_traversal               | 3.52 ms                                                                | 3.35 ms: 1.05x faster                                                   |
| richards                   | 67.2 ms                                                                | 64.7 ms: 1.04x faster                                                   |
| deltablue                  | 7.29 ms                                                                | 7.06 ms: 1.03x faster                                                   |
| chaos                      | 94.3 ms                                                                | 91.7 ms: 1.03x faster                                                   |
| deepcopy_reduce            | 3.46 us                                                                | 3.37 us: 1.03x faster                                                   |
| raytrace                   | 495 ms                                                                 | 483 ms: 1.02x faster                                                    |
| comprehensions             | 27.6 us                                                                | 26.9 us: 1.02x faster                                                   |
| pprint_safe_repr           | 961 ms                                                                 | 939 ms: 1.02x faster                                                    |
| scimark_monte_carlo        | 103 ms                                                                 | 101 ms: 1.02x faster                                                    |
| sqlglot_optimize           | 66.5 ms                                                                | 65.0 ms: 1.02x faster                                                   |
| nbody                      | 129 ms                                                                 | 126 ms: 1.02x faster                                                    |
| go                         | 231 ms                                                                 | 226 ms: 1.02x faster                                                    |
| json_dumps                 | 14.1 ms                                                                | 13.8 ms: 1.02x faster                                                   |
| mdp                        | 2.73 sec                                                               | 2.67 sec: 1.02x faster                                                  |
| subparsers                 | 28.6 ms                                                                | 28.0 ms: 1.02x faster                                                   |
| logging_silent             | 187 ns                                                                 | 184 ns: 1.02x faster                                                    |
| pprint_pformat             | 1.99 sec                                                               | 1.95 sec: 1.02x faster                                                  |
| xml_etree_iterparse        | 90.0 ms                                                                | 88.4 ms: 1.02x faster                                                   |
| 2to3                       | 345 ms                                                                 | 339 ms: 1.02x faster                                                    |
| bpe_tokeniser              | 4.98 sec                                                               | 4.90 sec: 1.02x faster                                                  |
| sqlglot_parse              | 2.28 ms                                                                | 2.25 ms: 1.02x faster                                                   |
| coroutines                 | 23.1 ms                                                                | 22.8 ms: 1.02x faster                                                   |
| sphinx                     | 1.16 sec                                                               | 1.14 sec: 1.01x faster                                                  |
| scimark_sor                | 201 ms                                                                 | 199 ms: 1.01x faster                                                    |
| hexiom                     | 9.22 ms                                                                | 9.11 ms: 1.01x faster                                                   |
| fannkuch                   | 480 ms                                                                 | 474 ms: 1.01x faster                                                    |
| sqlalchemy_declarative     | 183 ms                                                                 | 181 ms: 1.01x faster                                                    |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                                    |
| crypto_pyaes               | 90.2 ms                                                                | 89.2 ms: 1.01x faster                                                   |
| sympy_str                  | 354 ms                                                                 | 350 ms: 1.01x faster                                                    |
| genshi_xml                 | 62.7 ms                                                                | 62.0 ms: 1.01x faster                                                   |
| richards_super             | 74.6 ms                                                                | 73.8 ms: 1.01x faster                                                   |
| sympy_integrate            | 25.0 ms                                                                | 24.8 ms: 1.01x faster                                                   |
| many_optionals             | 1.24 ms                                                                | 1.22 ms: 1.01x faster                                                   |
| sympy_sum                  | 194 ms                                                                 | 192 ms: 1.01x faster                                                    |
| async_tree_memoization     | 431 ms                                                                 | 427 ms: 1.01x faster                                                    |
| thrift                     | 1.01 ms                                                                | 999 us: 1.01x faster                                                    |
| telco                      | 8.65 ms                                                                | 8.58 ms: 1.01x faster                                                   |
| float                      | 106 ms                                                                 | 105 ms: 1.01x faster                                                    |
| pickle_pure_python         | 493 us                                                                 | 489 us: 1.01x faster                                                    |
| sqlglot_transpile          | 2.64 ms                                                                | 2.62 ms: 1.01x faster                                                   |
| sqlglot_normalize          | 132 ms                                                                 | 131 ms: 1.01x faster                                                    |
| python_startup             | 15.7 ms                                                                | 15.6 ms: 1.01x faster                                                   |
| python_startup_no_site     | 9.82 ms                                                                | 9.76 ms: 1.01x faster                                                   |
| deepcopy_memo              | 40.6 us                                                                | 40.4 us: 1.01x faster                                                   |
| dulwich_log                | 90.4 ms                                                                | 89.9 ms: 1.01x faster                                                   |
| xml_etree_process          | 73.3 ms                                                                | 73.0 ms: 1.00x faster                                                   |
| xml_etree_generate         | 97.3 ms                                                                | 96.9 ms: 1.00x faster                                                   |
| async_tree_cpu_io_mixed    | 598 ms                                                                 | 601 ms: 1.01x slower                                                    |
| scimark_fft                | 373 ms                                                                 | 376 ms: 1.01x slower                                                    |
| regex_v8                   | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                                   |
| pyflate                    | 620 ms                                                                 | 625 ms: 1.01x slower                                                    |
| tomli_loads                | 2.32 sec                                                               | 2.34 sec: 1.01x slower                                                  |
| logging_simple             | 8.83 us                                                                | 8.96 us: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                 | 574 ms: 1.02x slower                                                    |
| regex_effbot               | 2.69 ms                                                                | 2.74 ms: 1.02x slower                                                   |
| logging_format             | 9.81 us                                                                | 10.0 us: 1.02x slower                                                   |
| json_loads                 | 28.6 us                                                                | 29.3 us: 1.02x slower                                                   |
| json                       | 5.10 ms                                                                | 5.22 ms: 1.02x slower                                                   |
| generators                 | 38.4 ms                                                                | 39.4 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 5.45 ms                                                                | 5.59 ms: 1.03x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.03x slower                                                    |
| async_generators           | 430 ms                                                                 | 447 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (29): pylint, sympy_expand, sqlite_synth, meteor_contest, async_tree_none_tg, async_tree_io_tg, unpickle_pure_python, docutils, regex_compile, coverage, shortest_path, deepcopy, asyncio_websockets, async_tree_none, html5lib, async_tree_io, k_core, scimark_lu, django_template, mako, bench_thread_pool, genshi_text, nqueens, sqlalchemy_imperative, async_tree_memoization_tg, pathlib, pycparser, typing_runtime_protocols, connected_components

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x