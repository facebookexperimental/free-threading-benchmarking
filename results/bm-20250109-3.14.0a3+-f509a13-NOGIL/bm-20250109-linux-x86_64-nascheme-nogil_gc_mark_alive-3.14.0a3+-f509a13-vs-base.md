# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.058x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 614 ms                                                                 | 681 ms: 1.11x slower                                                    |
| docutils       | 4.46 sec                                                               | 4.92 sec: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 983 ms                                                                 | 1.04 sec: 1.05x slower                                                  |
| async_tree_none_tg         | 412 ms                                                                 | 436 ms: 1.06x slower                                                    |
| async_generators           | 625 ms                                                                 | 665 ms: 1.06x slower                                                    |
| async_tree_memoization     | 604 ms                                                                 | 652 ms: 1.08x slower                                                    |
| coroutines                 | 34.7 ms                                                                | 37.4 ms: 1.08x slower                                                   |
| async_tree_none            | 517 ms                                                                 | 565 ms: 1.09x slower                                                    |
| async_tree_cpu_io_mixed_tg | 771 ms                                                                 | 860 ms: 1.11x slower                                                    |
| asyncio_websockets         | 714 ms                                                                 | 830 ms: 1.16x slower                                                    |
| async_tree_io              | 966 ms                                                                 | 1.14 sec: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 137 ms                                                                 | 146 ms: 1.07x slower                                                    |
| nbody          | 178 ms                                                                 | 197 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 316 ms                                                                 | 278 ms: 1.13x faster                                                    |
| regex_effbot   | 4.49 ms                                                                | 4.84 ms: 1.08x slower                                                   |
| regex_compile  | 210 ms                                                                 | 234 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 445 us                                                                 | 468 us: 1.05x slower                                                    |
| json_loads           | 38.7 us                                                                | 41.7 us: 1.08x slower                                                   |
| xml_etree_process    | 100 ms                                                                 | 108 ms: 1.08x slower                                                    |
| tomli_loads          | 2.93 sec                                                               | 3.23 sec: 1.10x slower                                                  |
| xml_etree_parse      | 229 ms                                                                 | 256 ms: 1.12x slower                                                    |
| json_dumps           | 16.3 ms                                                                | 19.0 ms: 1.17x slower                                                   |
| pickle_pure_python   | 643 us                                                                 | 813 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 20.0 ms                                                                | 27.2 ms: 1.36x slower                                                   |
| python_startup         | 30.6 ms                                                                | 42.9 ms: 1.40x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.38x slower                                                            |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): mako, django_template, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna                  | 316 ms                                                                 | 278 ms: 1.13x faster                                                    |
| create_gc_cycles           | 4.47 ms                                                                | 3.97 ms: 1.13x faster                                                   |
| sqlglot_parse              | 3.31 ms                                                                | 3.12 ms: 1.06x faster                                                   |
| scimark_monte_carlo        | 140 ms                                                                 | 133 ms: 1.05x faster                                                    |
| hexiom                     | 13.0 ms                                                                | 12.4 ms: 1.05x faster                                                   |
| unpickle_pure_python       | 445 us                                                                 | 468 us: 1.05x slower                                                    |
| async_tree_io_tg           | 983 ms                                                                 | 1.04 sec: 1.05x slower                                                  |
| nqueens                    | 137 ms                                                                 | 145 ms: 1.06x slower                                                    |
| async_tree_none_tg         | 412 ms                                                                 | 436 ms: 1.06x slower                                                    |
| coverage                   | 134 ms                                                                 | 142 ms: 1.06x slower                                                    |
| async_generators           | 625 ms                                                                 | 665 ms: 1.06x slower                                                    |
| float                      | 137 ms                                                                 | 146 ms: 1.07x slower                                                    |
| deltablue                  | 9.66 ms                                                                | 10.3 ms: 1.07x slower                                                   |
| deepcopy_reduce            | 4.33 us                                                                | 4.63 us: 1.07x slower                                                   |
| logging_format             | 12.3 us                                                                | 13.2 us: 1.07x slower                                                   |
| typing_runtime_protocols   | 271 us                                                                 | 290 us: 1.07x slower                                                    |
| crypto_pyaes               | 124 ms                                                                 | 134 ms: 1.07x slower                                                    |
| json_loads                 | 38.7 us                                                                | 41.7 us: 1.08x slower                                                   |
| sqlglot_normalize          | 163 ms                                                                 | 175 ms: 1.08x slower                                                    |
| sympy_sum                  | 272 ms                                                                 | 292 ms: 1.08x slower                                                    |
| regex_effbot               | 4.49 ms                                                                | 4.84 ms: 1.08x slower                                                   |
| async_tree_memoization     | 604 ms                                                                 | 652 ms: 1.08x slower                                                    |
| coroutines                 | 34.7 ms                                                                | 37.4 ms: 1.08x slower                                                   |
| fannkuch                   | 639 ms                                                                 | 691 ms: 1.08x slower                                                    |
| xml_etree_process          | 100 ms                                                                 | 108 ms: 1.08x slower                                                    |
| scimark_fft                | 518 ms                                                                 | 563 ms: 1.09x slower                                                    |
| generators                 | 51.5 ms                                                                | 56.0 ms: 1.09x slower                                                   |
| subparsers                 | 45.4 ms                                                                | 49.4 ms: 1.09x slower                                                   |
| async_tree_none            | 517 ms                                                                 | 565 ms: 1.09x slower                                                    |
| pathlib                    | 30.7 ms                                                                | 33.7 ms: 1.10x slower                                                   |
| sqlglot_transpile          | 3.78 ms                                                                | 4.15 ms: 1.10x slower                                                   |
| meteor_contest             | 177 ms                                                                 | 196 ms: 1.10x slower                                                    |
| docutils                   | 4.46 sec                                                               | 4.92 sec: 1.10x slower                                                  |
| tomli_loads                | 2.93 sec                                                               | 3.23 sec: 1.10x slower                                                  |
| richards                   | 79.9 ms                                                                | 88.2 ms: 1.10x slower                                                   |
| nbody                      | 178 ms                                                                 | 197 ms: 1.11x slower                                                    |
| 2to3                       | 614 ms                                                                 | 681 ms: 1.11x slower                                                    |
| connected_components       | 963 ms                                                                 | 1.07 sec: 1.11x slower                                                  |
| async_tree_cpu_io_mixed_tg | 771 ms                                                                 | 860 ms: 1.11x slower                                                    |
| xml_etree_parse            | 229 ms                                                                 | 256 ms: 1.12x slower                                                    |
| scimark_sparse_mat_mult    | 8.37 ms                                                                | 9.34 ms: 1.12x slower                                                   |
| regex_compile              | 210 ms                                                                 | 234 ms: 1.12x slower                                                    |
| k_core                     | 4.41 sec                                                               | 4.93 sec: 1.12x slower                                                  |
| shortest_path              | 1.04 sec                                                               | 1.17 sec: 1.13x slower                                                  |
| raytrace                   | 570 ms                                                                 | 644 ms: 1.13x slower                                                    |
| deepcopy                   | 414 us                                                                 | 470 us: 1.14x slower                                                    |
| pprint_safe_repr           | 1.19 sec                                                               | 1.36 sec: 1.14x slower                                                  |
| pycparser                  | 1.73 sec                                                               | 1.98 sec: 1.14x slower                                                  |
| mdp                        | 4.24 sec                                                               | 4.86 sec: 1.14x slower                                                  |
| deepcopy_memo              | 52.0 us                                                                | 59.6 us: 1.15x slower                                                   |
| json                       | 6.95 ms                                                                | 7.98 ms: 1.15x slower                                                   |
| bench_mp_pool              | 88.0 ms                                                                | 101 ms: 1.15x slower                                                    |
| go                         | 273 ms                                                                 | 314 ms: 1.15x slower                                                    |
| sqlglot_optimize           | 82.8 ms                                                                | 95.7 ms: 1.15x slower                                                   |
| chaos                      | 119 ms                                                                 | 138 ms: 1.16x slower                                                    |
| asyncio_websockets         | 714 ms                                                                 | 830 ms: 1.16x slower                                                    |
| json_dumps                 | 16.3 ms                                                                | 19.0 ms: 1.17x slower                                                   |
| bpe_tokeniser              | 7.57 sec                                                               | 8.87 sec: 1.17x slower                                                  |
| async_tree_io              | 966 ms                                                                 | 1.14 sec: 1.18x slower                                                  |
| gc_traversal               | 8.54 ms                                                                | 10.2 ms: 1.19x slower                                                   |
| sympy_str                  | 433 ms                                                                 | 520 ms: 1.20x slower                                                    |
| logging_simple             | 10.5 us                                                                | 13.1 us: 1.24x slower                                                   |
| pickle_pure_python         | 643 us                                                                 | 813 us: 1.26x slower                                                    |
| bench_thread_pool          | 4.59 ms                                                                | 5.81 ms: 1.27x slower                                                   |
| sqlalchemy_declarative     | 249 ms                                                                 | 325 ms: 1.30x slower                                                    |
| python_startup_no_site     | 20.0 ms                                                                | 27.2 ms: 1.36x slower                                                   |
| dulwich_log                | 111 ms                                                                 | 155 ms: 1.40x slower                                                    |
| python_startup             | 30.6 ms                                                                | 42.9 ms: 1.40x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (28): thrift, many_optionals, pidigits, spectral_norm, async_tree_memoization_tg, logging_silent, regex_v8, pyflate, async_tree_cpu_io_mixed, sphinx, html5lib, sqlite_synth, telco, sympy_expand, pprint_pformat, scimark_lu, xml_etree_generate, mako, xml_etree_iterparse, sqlalchemy_imperative, comprehensions, django_template, richards_super, scimark_sor, genshi_text, sympy_integrate, genshi_xml, pylint

- Geometric mean (including insignificant results): 1.058x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.00x