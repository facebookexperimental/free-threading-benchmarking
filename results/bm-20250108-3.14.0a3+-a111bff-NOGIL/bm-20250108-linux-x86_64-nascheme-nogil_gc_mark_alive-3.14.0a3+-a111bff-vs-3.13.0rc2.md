# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.150x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 600 ms: 1.35x slower                                                    |
| docutils       | 4.01 sec                                                     | 4.23 sec: 1.05x slower                                                  |
| html5lib       | 92.6 ms                                                      | 108 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                        | 1.18x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 960 ms: 1.46x faster                                                    |
| async_tree_io              | 1.39 sec                                                     | 1.07 sec: 1.30x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 542 ms: 1.24x faster                                                    |
| async_tree_none            | 572 ms                                                       | 495 ms: 1.16x faster                                                    |
| async_tree_none_tg         | 504 ms                                                       | 439 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 748 ms: 1.14x faster                                                    |
| async_tree_memoization     | 709 ms                                                       | 634 ms: 1.12x faster                                                    |
| asyncio_websockets         | 766 ms                                                       | 738 ms: 1.04x faster                                                    |
| async_generators           | 567 ms                                                       | 602 ms: 1.06x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.13x faster                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 131 ms: 1.13x slower                                                    |
| nbody          | 119 ms                                                       | 173 ms: 1.46x slower                                                    |
| Geometric mean | (ref)                                                        | 1.17x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.27 ms: 1.11x faster                                                   |
| regex_dna      | 282 ms                                                       | 321 ms: 1.14x slower                                                    |
| regex_compile  | 182 ms                                                       | 221 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                        | 1.07x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 135 ms: 1.31x faster                                                    |
| json_loads           | 34.3 us                                                      | 36.8 us: 1.07x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.03 sec: 1.09x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 137 ms: 1.12x slower                                                    |
| json_dumps           | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 113 ms: 1.32x slower                                                    |
| unpickle_pure_python | 290 us                                                       | 389 us: 1.34x slower                                                    |
| pickle_pure_python   | 416 us                                                       | 702 us: 1.69x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.2 ms: 1.32x slower                                                   |
| python_startup         | 22.4 ms                                                      | 32.7 ms: 1.46x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 91.2 ms: 1.27x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 41.2 ms: 1.30x slower                                                   |
| django_template | 44.3 ms                                                      | 70.3 ms: 1.59x slower                                                   |
| mako            | 15.9 ms                                                      | 25.7 ms: 1.61x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.43x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 960 ms: 1.46x faster                                                    |
| xml_etree_iterparse        | 177 ms                                                       | 135 ms: 1.31x faster                                                    |
| async_tree_io              | 1.39 sec                                                     | 1.07 sec: 1.30x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 542 ms: 1.24x faster                                                    |
| deepcopy                   | 498 us                                                       | 426 us: 1.17x faster                                                    |
| async_tree_none            | 572 ms                                                       | 495 ms: 1.16x faster                                                    |
| async_tree_none_tg         | 504 ms                                                       | 439 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 748 ms: 1.14x faster                                                    |
| sqlite_synth               | 3.99 us                                                      | 3.51 us: 1.13x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 634 ms: 1.12x faster                                                    |
| regex_effbot               | 4.74 ms                                                      | 4.27 ms: 1.11x faster                                                   |
| telco                      | 12.2 ms                                                      | 11.6 ms: 1.05x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 738 ms: 1.04x faster                                                    |
| docutils                   | 4.01 sec                                                     | 4.23 sec: 1.05x slower                                                  |
| async_generators           | 567 ms                                                       | 602 ms: 1.06x slower                                                    |
| pycparser                  | 1.57 sec                                                     | 1.67 sec: 1.06x slower                                                  |
| json_loads                 | 34.3 us                                                      | 36.8 us: 1.07x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.03 sec: 1.09x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 4.56 us: 1.11x slower                                                   |
| pylint                     | 470 ms                                                       | 526 ms: 1.12x slower                                                    |
| json                       | 6.51 ms                                                      | 7.29 ms: 1.12x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 137 ms: 1.12x slower                                                    |
| float                      | 116 ms                                                       | 131 ms: 1.13x slower                                                    |
| sympy_expand               | 601 ms                                                       | 682 ms: 1.13x slower                                                    |
| regex_dna                  | 282 ms                                                       | 321 ms: 1.14x slower                                                    |
| mdp                        | 3.80 sec                                                     | 4.40 sec: 1.16x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 108 ms: 1.16x slower                                                    |
| scimark_fft                | 473 ms                                                       | 558 ms: 1.18x slower                                                    |
| thrift                     | 1.10 ms                                                      | 1.31 ms: 1.19x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 2.89 ms: 1.20x slower                                                   |
| richards                   | 65.5 ms                                                      | 78.5 ms: 1.20x slower                                                   |
| logging_simple             | 8.56 us                                                      | 10.3 us: 1.20x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 36.4 ms: 1.20x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.17 ms: 1.21x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 255 ms: 1.21x slower                                                    |
| regex_compile              | 182 ms                                                       | 221 ms: 1.21x slower                                                    |
| dulwich_log                | 93.7 ms                                                      | 114 ms: 1.21x slower                                                    |
| bpe_tokeniser              | 6.28 sec                                                     | 7.64 sec: 1.22x slower                                                  |
| coverage                   | 107 ms                                                       | 131 ms: 1.22x slower                                                    |
| pprint_safe_repr           | 987 ms                                                       | 1.21 sec: 1.23x slower                                                  |
| meteor_contest             | 150 ms                                                       | 184 ms: 1.23x slower                                                    |
| fannkuch                   | 547 ms                                                       | 674 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 226 us                                                       | 279 us: 1.23x slower                                                    |
| nqueens                    | 112 ms                                                       | 138 ms: 1.24x slower                                                    |
| crypto_pyaes               | 100 ms                                                       | 124 ms: 1.24x slower                                                    |
| scimark_sor                | 179 ms                                                       | 222 ms: 1.24x slower                                                    |
| bench_thread_pool          | 2.89 ms                                                      | 3.61 ms: 1.25x slower                                                   |
| richards_super             | 73.2 ms                                                      | 91.6 ms: 1.25x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 94.0 ms: 1.26x slower                                                   |
| sympy_str                  | 379 ms                                                       | 478 ms: 1.26x slower                                                    |
| genshi_xml                 | 72.1 ms                                                      | 91.2 ms: 1.27x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 41.2 ms: 1.30x slower                                                   |
| pyflate                    | 664 ms                                                       | 868 ms: 1.31x slower                                                    |
| xml_etree_process          | 85.9 ms                                                      | 113 ms: 1.32x slower                                                    |
| python_startup_no_site     | 15.3 ms                                                      | 20.2 ms: 1.32x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 389 us: 1.34x slower                                                    |
| 2to3                       | 445 ms                                                       | 600 ms: 1.35x slower                                                    |
| chaos                      | 83.6 ms                                                      | 113 ms: 1.35x slower                                                    |
| sqlglot_normalize          | 140 ms                                                       | 191 ms: 1.36x slower                                                    |
| pprint_pformat             | 1.94 sec                                                     | 2.66 sec: 1.37x slower                                                  |
| generators                 | 40.0 ms                                                      | 54.8 ms: 1.37x slower                                                   |
| logging_format             | 9.24 us                                                      | 12.7 us: 1.38x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 202 ms: 1.38x slower                                                    |
| hexiom                     | 8.11 ms                                                      | 11.4 ms: 1.40x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 129 ms: 1.42x slower                                                    |
| go                         | 191 ms                                                       | 272 ms: 1.42x slower                                                    |
| comprehensions             | 22.2 us                                                      | 31.8 us: 1.43x slower                                                   |
| nbody                      | 119 ms                                                       | 173 ms: 1.46x slower                                                    |
| python_startup             | 22.4 ms                                                      | 32.7 ms: 1.46x slower                                                   |
| gc_traversal               | 5.70 ms                                                      | 8.36 ms: 1.47x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 3.44 ms: 1.57x slower                                                   |
| django_template            | 44.3 ms                                                      | 70.3 ms: 1.59x slower                                                   |
| mako                       | 15.9 ms                                                      | 25.7 ms: 1.61x slower                                                   |
| raytrace                   | 344 ms                                                       | 563 ms: 1.64x slower                                                    |
| pickle_pure_python         | 416 us                                                       | 702 us: 1.69x slower                                                    |
| logging_silent             | 130 ns                                                       | 224 ns: 1.72x slower                                                    |
| sqlglot_parse              | 1.76 ms                                                      | 3.07 ms: 1.75x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 9.71 ms: 2.19x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 91.2 ms: 4.88x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.20x slower                                                            |

Benchmark hidden because not significant (8): xml_etree_parse, pidigits, async_tree_cpu_io_mixed, spectral_norm, deepcopy_memo, coroutines, regex_v8, pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250108-3.14.0a3+-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.150x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.33x