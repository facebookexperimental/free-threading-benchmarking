# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.017x faster
- HPT reliability: 67.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 4.46 sec                                                               | 4.23 sec: 1.05x faster                                                  |
| html5lib       | 129 ms                                                                 | 108 ms: 1.20x faster                                                    |
| sphinx         | 1.73 sec                                                               | 1.60 sec: 1.08x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                 | 34.7 ms                                                                | 31.4 ms: 1.11x faster                                                   |
| async_tree_memoization_tg  | 593 ms                                                                 | 542 ms: 1.09x faster                                                    |
| async_tree_none            | 517 ms                                                                 | 495 ms: 1.05x faster                                                    |
| async_generators           | 625 ms                                                                 | 602 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg | 771 ms                                                                 | 748 ms: 1.03x faster                                                    |
| asyncio_websockets         | 714 ms                                                                 | 738 ms: 1.03x slower                                                    |
| async_tree_memoization     | 604 ms                                                                 | 634 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed    | 821 ms                                                                 | 867 ms: 1.06x slower                                                    |
| async_tree_none_tg         | 412 ms                                                                 | 439 ms: 1.07x slower                                                    |
| async_tree_io              | 966 ms                                                                 | 1.07 sec: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 137 ms                                                                 | 131 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 4.49 ms                                                                | 4.27 ms: 1.05x faster                                                   |
| regex_compile  | 210 ms                                                                 | 221 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 445 us                                                                 | 389 us: 1.14x faster                                                    |
| xml_etree_iterparse  | 148 ms                                                                 | 135 ms: 1.10x faster                                                    |
| json_loads           | 38.7 us                                                                | 36.8 us: 1.05x faster                                                   |
| tomli_loads          | 2.93 sec                                                               | 3.03 sec: 1.03x slower                                                  |
| pickle_pure_python   | 643 us                                                                 | 702 us: 1.09x slower                                                    |
| json_dumps           | 16.3 ms                                                                | 18.1 ms: 1.11x slower                                                   |
| xml_etree_process    | 100 ms                                                                 | 113 ms: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup | 30.6 ms                                                                | 32.7 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 27.1 ms                                                                | 25.7 ms: 1.05x faster                                                   |
| django_template | 59.7 ms                                                                | 70.3 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles           | 4.47 ms                                                                | 2.89 ms: 1.55x faster                                                   |
| bench_thread_pool          | 4.59 ms                                                                | 3.61 ms: 1.27x faster                                                   |
| html5lib                   | 129 ms                                                                 | 108 ms: 1.20x faster                                                    |
| sqlite_synth               | 4.21 us                                                                | 3.51 us: 1.20x faster                                                   |
| unpickle_pure_python       | 445 us                                                                 | 389 us: 1.14x faster                                                    |
| hexiom                     | 13.0 ms                                                                | 11.4 ms: 1.14x faster                                                   |
| subparsers                 | 45.4 ms                                                                | 40.6 ms: 1.12x faster                                                   |
| thrift                     | 1.46 ms                                                                | 1.31 ms: 1.12x faster                                                   |
| comprehensions             | 35.3 us                                                                | 31.8 us: 1.11x faster                                                   |
| coroutines                 | 34.7 ms                                                                | 31.4 ms: 1.11x faster                                                   |
| many_optionals             | 1.44 ms                                                                | 1.31 ms: 1.10x faster                                                   |
| sqlglot_transpile          | 3.78 ms                                                                | 3.44 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 148 ms                                                                 | 135 ms: 1.10x faster                                                    |
| async_tree_memoization_tg  | 593 ms                                                                 | 542 ms: 1.09x faster                                                    |
| spectral_norm              | 167 ms                                                                 | 153 ms: 1.09x faster                                                    |
| sympy_expand               | 743 ms                                                                 | 682 ms: 1.09x faster                                                    |
| scimark_monte_carlo        | 140 ms                                                                 | 129 ms: 1.09x faster                                                    |
| scimark_sor                | 240 ms                                                                 | 222 ms: 1.08x faster                                                    |
| sphinx                     | 1.73 sec                                                               | 1.60 sec: 1.08x faster                                                  |
| sqlglot_parse              | 3.31 ms                                                                | 3.07 ms: 1.08x faster                                                   |
| pyflate                    | 928 ms                                                                 | 868 ms: 1.07x faster                                                    |
| sympy_sum                  | 272 ms                                                                 | 255 ms: 1.07x faster                                                    |
| richards_super             | 97.0 ms                                                                | 91.6 ms: 1.06x faster                                                   |
| logging_silent             | 237 ns                                                                 | 224 ns: 1.06x faster                                                    |
| chaos                      | 119 ms                                                                 | 113 ms: 1.06x faster                                                    |
| docutils                   | 4.46 sec                                                               | 4.23 sec: 1.05x faster                                                  |
| mako                       | 27.1 ms                                                                | 25.7 ms: 1.05x faster                                                   |
| json_loads                 | 38.7 us                                                                | 36.8 us: 1.05x faster                                                   |
| regex_effbot               | 4.49 ms                                                                | 4.27 ms: 1.05x faster                                                   |
| float                      | 137 ms                                                                 | 131 ms: 1.05x faster                                                    |
| async_tree_none            | 517 ms                                                                 | 495 ms: 1.05x faster                                                    |
| async_generators           | 625 ms                                                                 | 602 ms: 1.04x faster                                                    |
| pycparser                  | 1.73 sec                                                               | 1.67 sec: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 771 ms                                                                 | 748 ms: 1.03x faster                                                    |
| asyncio_websockets         | 714 ms                                                                 | 738 ms: 1.03x slower                                                    |
| tomli_loads                | 2.93 sec                                                               | 3.03 sec: 1.03x slower                                                  |
| mdp                        | 4.24 sec                                                               | 4.40 sec: 1.04x slower                                                  |
| shortest_path              | 1.04 sec                                                               | 1.08 sec: 1.04x slower                                                  |
| json                       | 6.95 ms                                                                | 7.29 ms: 1.05x slower                                                   |
| async_tree_memoization     | 604 ms                                                                 | 634 ms: 1.05x slower                                                    |
| deepcopy_reduce            | 4.33 us                                                                | 4.56 us: 1.05x slower                                                   |
| fannkuch                   | 639 ms                                                                 | 674 ms: 1.05x slower                                                    |
| regex_compile              | 210 ms                                                                 | 221 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed    | 821 ms                                                                 | 867 ms: 1.06x slower                                                    |
| generators                 | 51.5 ms                                                                | 54.8 ms: 1.06x slower                                                   |
| async_tree_none_tg         | 412 ms                                                                 | 439 ms: 1.07x slower                                                    |
| python_startup             | 30.6 ms                                                                | 32.7 ms: 1.07x slower                                                   |
| scimark_fft                | 518 ms                                                                 | 558 ms: 1.08x slower                                                    |
| pickle_pure_python         | 643 us                                                                 | 702 us: 1.09x slower                                                    |
| sqlalchemy_imperative      | 36.3 ms                                                                | 39.8 ms: 1.10x slower                                                   |
| sympy_str                  | 433 ms                                                                 | 478 ms: 1.10x slower                                                    |
| async_tree_io              | 966 ms                                                                 | 1.07 sec: 1.11x slower                                                  |
| json_dumps                 | 16.3 ms                                                                | 18.1 ms: 1.11x slower                                                   |
| xml_etree_process          | 100 ms                                                                 | 113 ms: 1.13x slower                                                    |
| sqlglot_optimize           | 82.8 ms                                                                | 94.0 ms: 1.13x slower                                                   |
| sqlglot_normalize          | 163 ms                                                                 | 191 ms: 1.17x slower                                                    |
| django_template            | 59.7 ms                                                                | 70.3 ms: 1.18x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (39): xml_etree_generate, regex_v8, deepcopy_memo, xml_etree_parse, nbody, async_tree_io_tg, scimark_sparse_mat_mult, logging_simple, 2to3, coverage, gc_traversal, telco, richards, sympy_integrate, genshi_xml, pidigits, raytrace, genshi_text, connected_components, go, crypto_pyaes, deltablue, nqueens, k_core, bpe_tokeniser, pathlib, python_startup_no_site, pprint_safe_repr, regex_dna, pprint_pformat, scimark_lu, dulwich_log, deepcopy, sqlalchemy_declarative, pylint, typing_runtime_protocols, bench_mp_pool, meteor_contest, logging_format

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 67.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x