# Results vs. 3.13.0rc2

- fork: mpage
- ref: revert_c3ae5c9
- machine: linux-x86_64
- commit hash: 3edc57c
- commit date: 2025-02-01
- overall geometric mean: 1.082x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 304 ms: 1.17x slower                                            |
| docutils       | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                          |
| html5lib       | 67.0 ms                                                      | 70.9 ms: 1.06x slower                                           |
| Geometric mean | (ref)                                                        | 1.10x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                            |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                            |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.33x faster                                            |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 326 ms: 1.27x faster                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 506 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 540 ms: 1.23x faster                                            |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.22x faster                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                           |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                            |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                            |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                            |
| float          | 77.5 ms                                                      | 76.7 ms: 1.01x faster                                           |
| nbody          | 85.1 ms                                                      | 137 ms: 1.61x slower                                            |
| Geometric mean | (ref)                                                        | 1.12x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                           |
| regex_dna      | 180 ms                                                       | 181 ms: 1.00x slower                                            |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                           |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                            |
| Geometric mean | (ref)                                                        | 1.02x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.5 ms: 1.08x faster                                           |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                            |
| xml_etree_generate   | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                           |
| xml_etree_process    | 59.3 ms                                                      | 68.9 ms: 1.16x slower                                           |
| json_loads           | 27.0 us                                                      | 31.6 us: 1.17x slower                                           |
| unpickle_pure_python | 210 us                                                       | 246 us: 1.17x slower                                            |
| tomli_loads          | 2.01 sec                                                     | 2.38 sec: 1.19x slower                                          |
| json_dumps           | 10.5 ms                                                      | 12.9 ms: 1.23x slower                                           |
| pickle_pure_python   | 294 us                                                       | 374 us: 1.27x slower                                            |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.64 ms: 1.30x slower                                           |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                           |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 42.1 ms: 1.23x slower                                           |
| genshi_xml      | 48.8 ms                                                      | 61.1 ms: 1.25x slower                                           |
| genshi_text     | 21.5 ms                                                      | 28.3 ms: 1.31x slower                                           |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                           |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.66 ms: 1.89x faster                                           |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                            |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                            |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.33x faster                                            |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 326 ms: 1.27x faster                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 506 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 540 ms: 1.23x faster                                            |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.22x faster                                            |
| deepcopy                   | 355 us                                                       | 312 us: 1.14x faster                                            |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                            |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.5 ms: 1.08x faster                                           |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                           |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                            |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.03x faster                                           |
| go                         | 141 ms                                                       | 137 ms: 1.03x faster                                            |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                           |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                            |
| float                      | 77.5 ms                                                      | 76.7 ms: 1.01x faster                                           |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                            |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                            |
| regex_dna                  | 180 ms                                                       | 181 ms: 1.00x slower                                            |
| deepcopy_reduce            | 3.11 us                                                      | 3.23 us: 1.04x slower                                           |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                           |
| bpe_tokeniser              | 4.45 sec                                                     | 4.64 sec: 1.04x slower                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.40 ms: 1.05x slower                                           |
| html5lib                   | 67.0 ms                                                      | 70.9 ms: 1.06x slower                                           |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.06x slower                                          |
| logging_silent             | 103 ns                                                       | 109 ns: 1.07x slower                                            |
| docutils                   | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                          |
| telco                      | 7.82 ms                                                      | 8.61 ms: 1.10x slower                                           |
| json                       | 4.93 ms                                                      | 5.46 ms: 1.11x slower                                           |
| dulwich_log                | 74.8 ms                                                      | 82.9 ms: 1.11x slower                                           |
| scimark_fft                | 349 ms                                                       | 389 ms: 1.11x slower                                            |
| pprint_safe_repr           | 738 ms                                                       | 823 ms: 1.12x slower                                            |
| pyflate                    | 449 ms                                                       | 501 ms: 1.12x slower                                            |
| mdp                        | 2.36 sec                                                     | 2.64 sec: 1.12x slower                                          |
| xml_etree_generate         | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                           |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                            |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.13x slower                                            |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.13x slower                                          |
| generators                 | 28.8 ms                                                      | 33.3 ms: 1.16x slower                                           |
| sqlglot_optimize           | 52.7 ms                                                      | 61.2 ms: 1.16x slower                                           |
| xml_etree_process          | 59.3 ms                                                      | 68.9 ms: 1.16x slower                                           |
| json_loads                 | 27.0 us                                                      | 31.6 us: 1.17x slower                                           |
| unpickle_pure_python       | 210 us                                                       | 246 us: 1.17x slower                                            |
| 2to3                       | 260 ms                                                       | 304 ms: 1.17x slower                                            |
| thrift                     | 778 us                                                       | 922 us: 1.18x slower                                            |
| logging_format             | 6.84 us                                                      | 8.10 us: 1.18x slower                                           |
| logging_simple             | 6.16 us                                                      | 7.30 us: 1.19x slower                                           |
| coverage                   | 83.0 ms                                                      | 98.5 ms: 1.19x slower                                           |
| tomli_loads                | 2.01 sec                                                     | 2.38 sec: 1.19x slower                                          |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.19x slower                                            |
| chaos                      | 57.3 ms                                                      | 68.6 ms: 1.20x slower                                           |
| sympy_expand               | 457 ms                                                       | 550 ms: 1.20x slower                                            |
| comprehensions             | 16.5 us                                                      | 19.9 us: 1.21x slower                                           |
| scimark_lu                 | 113 ms                                                       | 137 ms: 1.22x slower                                            |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                           |
| sympy_str                  | 275 ms                                                       | 337 ms: 1.23x slower                                            |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.23x slower                                           |
| json_dumps                 | 10.5 ms                                                      | 12.9 ms: 1.23x slower                                           |
| nqueens                    | 78.6 ms                                                      | 96.6 ms: 1.23x slower                                           |
| django_template            | 34.1 ms                                                      | 42.1 ms: 1.23x slower                                           |
| hexiom                     | 5.99 ms                                                      | 7.41 ms: 1.24x slower                                           |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.83 ms: 1.24x slower                                           |
| richards                   | 45.2 ms                                                      | 56.5 ms: 1.25x slower                                           |
| genshi_xml                 | 48.8 ms                                                      | 61.1 ms: 1.25x slower                                           |
| sqlglot_parse              | 1.25 ms                                                      | 1.58 ms: 1.27x slower                                           |
| pickle_pure_python         | 294 us                                                       | 374 us: 1.27x slower                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 83.1 ms: 1.27x slower                                           |
| richards_super             | 51.6 ms                                                      | 66.0 ms: 1.28x slower                                           |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                            |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                            |
| raytrace                   | 253 ms                                                       | 327 ms: 1.29x slower                                            |
| python_startup_no_site     | 7.39 ms                                                      | 9.64 ms: 1.30x slower                                           |
| crypto_pyaes               | 67.9 ms                                                      | 89.0 ms: 1.31x slower                                           |
| genshi_text                | 21.5 ms                                                      | 28.3 ms: 1.31x slower                                           |
| fannkuch                   | 370 ms                                                       | 493 ms: 1.33x slower                                            |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                           |
| python_startup             | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                           |
| deltablue                  | 3.12 ms                                                      | 4.67 ms: 1.49x slower                                           |
| nbody                      | 85.1 ms                                                      | 137 ms: 1.61x slower                                            |
| bench_thread_pool          | 919 us                                                       | 3.29 ms: 3.59x slower                                           |
| bench_mp_pool              | 11.0 ms                                                      | 91.1 ms: 8.29x slower                                           |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                    |

Benchmark hidden because not significant (2): pylint, deepcopy_memo
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250201-3.14.0a4+-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.082x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.33x