# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.002x faster
- HPT reliability: 82.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 345 ms                                                                 | 341 ms: 1.01x faster                                                    |
| sphinx         | 1.16 sec                                                               | 1.14 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 431 ms                                                                 | 425 ms: 1.01x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 349 ms: 1.01x faster                                                    |
| async_tree_none_tg         | 316 ms                                                                 | 313 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 598 ms                                                                 | 594 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                 | 567 ms: 1.01x slower                                                    |
| async_generators           | 430 ms                                                                 | 446 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (5): async_tree_io, coroutines, async_tree_io_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 192 ms: 1.03x faster                                                    |
| nbody          | 129 ms                                                                 | 127 ms: 1.01x faster                                                    |
| float          | 106 ms                                                                 | 106 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 176 ms: 1.03x faster                                                    |
| regex_v8       | 23.4 ms                                                                | 23.8 ms: 1.01x slower                                                   |
| regex_effbot   | 2.69 ms                                                                | 2.77 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.0 ms                                                                | 88.7 ms: 1.02x faster                                                   |
| json_dumps           | 14.1 ms                                                                | 13.9 ms: 1.01x faster                                                   |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                    |
| xml_etree_process    | 73.3 ms                                                                | 73.1 ms: 1.00x faster                                                   |
| unpickle_pure_python | 320 us                                                                 | 323 us: 1.01x slower                                                    |
| tomli_loads          | 2.32 sec                                                               | 2.36 sec: 1.02x slower                                                  |
| json_loads           | 28.6 us                                                                | 29.2 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 9.82 ms                                                                | 9.67 ms: 1.02x faster                                                   |
| python_startup         | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 49.4 ms                                                                | 48.9 ms: 1.01x faster                                                   |
| mako            | 17.1 ms                                                                | 17.2 ms: 1.01x slower                                                   |
| genshi_text     | 30.3 ms                                                                | 30.6 ms: 1.01x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles           | 1.84 ms                                                                | 1.43 ms: 1.28x faster                                                   |
| bench_mp_pool              | 100 ms                                                                 | 94.3 ms: 1.06x faster                                                   |
| gc_traversal               | 3.52 ms                                                                | 3.33 ms: 1.05x faster                                                   |
| regex_dna                  | 181 ms                                                                 | 176 ms: 1.03x faster                                                    |
| pidigits                   | 197 ms                                                                 | 192 ms: 1.03x faster                                                    |
| pprint_safe_repr           | 961 ms                                                                 | 939 ms: 1.02x faster                                                    |
| logging_silent             | 187 ns                                                                 | 183 ns: 1.02x faster                                                    |
| sqlglot_parse              | 2.28 ms                                                                | 2.24 ms: 1.02x faster                                                   |
| richards                   | 67.2 ms                                                                | 66.0 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.99 sec                                                               | 1.96 sec: 1.02x faster                                                  |
| sqlglot_optimize           | 66.5 ms                                                                | 65.4 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 90.0 ms                                                                | 88.7 ms: 1.02x faster                                                   |
| python_startup_no_site     | 9.82 ms                                                                | 9.67 ms: 1.02x faster                                                   |
| sphinx                     | 1.16 sec                                                               | 1.14 sec: 1.01x faster                                                  |
| json_dumps                 | 14.1 ms                                                                | 13.9 ms: 1.01x faster                                                   |
| python_startup             | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                   |
| async_tree_memoization     | 431 ms                                                                 | 425 ms: 1.01x faster                                                    |
| raytrace                   | 495 ms                                                                 | 489 ms: 1.01x faster                                                    |
| nbody                      | 129 ms                                                                 | 127 ms: 1.01x faster                                                    |
| meteor_contest             | 131 ms                                                                 | 129 ms: 1.01x faster                                                    |
| django_template            | 49.4 ms                                                                | 48.9 ms: 1.01x faster                                                   |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 349 ms: 1.01x faster                                                    |
| 2to3                       | 345 ms                                                                 | 341 ms: 1.01x faster                                                    |
| async_tree_none_tg         | 316 ms                                                                 | 313 ms: 1.01x faster                                                    |
| sqlglot_transpile          | 2.64 ms                                                                | 2.62 ms: 1.01x faster                                                   |
| comprehensions             | 27.6 us                                                                | 27.4 us: 1.01x faster                                                   |
| deepcopy_reduce            | 3.46 us                                                                | 3.43 us: 1.01x faster                                                   |
| crypto_pyaes               | 90.2 ms                                                                | 89.5 ms: 1.01x faster                                                   |
| sympy_integrate            | 25.0 ms                                                                | 24.9 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed    | 598 ms                                                                 | 594 ms: 1.01x faster                                                    |
| sympy_str                  | 354 ms                                                                 | 352 ms: 1.01x faster                                                    |
| dulwich_log                | 90.4 ms                                                                | 89.8 ms: 1.01x faster                                                   |
| shortest_path              | 547 ms                                                                 | 544 ms: 1.01x faster                                                    |
| sqlalchemy_declarative     | 183 ms                                                                 | 182 ms: 1.01x faster                                                    |
| hexiom                     | 9.22 ms                                                                | 9.18 ms: 1.00x faster                                                   |
| sqlglot_normalize          | 132 ms                                                                 | 132 ms: 1.00x faster                                                    |
| xml_etree_process          | 73.3 ms                                                                | 73.1 ms: 1.00x faster                                                   |
| go                         | 231 ms                                                                 | 230 ms: 1.00x faster                                                    |
| deepcopy_memo              | 40.6 us                                                                | 40.7 us: 1.00x slower                                                   |
| bpe_tokeniser              | 4.98 sec                                                               | 4.99 sec: 1.00x slower                                                  |
| float                      | 106 ms                                                                 | 106 ms: 1.00x slower                                                    |
| scimark_sor                | 201 ms                                                                 | 202 ms: 1.00x slower                                                    |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                 | 567 ms: 1.01x slower                                                    |
| mako                       | 17.1 ms                                                                | 17.2 ms: 1.01x slower                                                   |
| pycparser                  | 1.34 sec                                                               | 1.35 sec: 1.01x slower                                                  |
| deepcopy                   | 323 us                                                                 | 325 us: 1.01x slower                                                    |
| logging_simple             | 8.83 us                                                                | 8.90 us: 1.01x slower                                                   |
| unpickle_pure_python       | 320 us                                                                 | 323 us: 1.01x slower                                                    |
| fannkuch                   | 480 ms                                                                 | 484 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 201 us                                                                 | 203 us: 1.01x slower                                                    |
| genshi_text                | 30.3 ms                                                                | 30.6 ms: 1.01x slower                                                   |
| coverage                   | 97.6 ms                                                                | 98.8 ms: 1.01x slower                                                   |
| regex_v8                   | 23.4 ms                                                                | 23.8 ms: 1.01x slower                                                   |
| pathlib                    | 19.2 ms                                                                | 19.5 ms: 1.02x slower                                                   |
| tomli_loads                | 2.32 sec                                                               | 2.36 sec: 1.02x slower                                                  |
| json_loads                 | 28.6 us                                                                | 29.2 us: 1.02x slower                                                   |
| pyflate                    | 620 ms                                                                 | 635 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 5.45 ms                                                                | 5.59 ms: 1.03x slower                                                   |
| scimark_fft                | 373 ms                                                                 | 383 ms: 1.03x slower                                                    |
| json                       | 5.10 ms                                                                | 5.24 ms: 1.03x slower                                                   |
| nqueens                    | 95.3 ms                                                                | 98.0 ms: 1.03x slower                                                   |
| regex_effbot               | 2.69 ms                                                                | 2.77 ms: 1.03x slower                                                   |
| richards_super             | 74.6 ms                                                                | 77.0 ms: 1.03x slower                                                   |
| async_generators           | 430 ms                                                                 | 446 ms: 1.04x slower                                                    |
| mdp                        | 2.73 sec                                                               | 2.88 sec: 1.05x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 115 ms: 1.06x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (29): pylint, chaos, sqlite_synth, thrift, html5lib, async_tree_io, genshi_xml, sympy_expand, coroutines, async_tree_io_tg, subparsers, sympy_sum, pickle_pure_python, xml_etree_generate, asyncio_websockets, scimark_monte_carlo, regex_compile, connected_components, telco, scimark_lu, k_core, many_optionals, docutils, bench_thread_pool, logging_format, deltablue, generators, async_tree_memoization_tg, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 82.70% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x