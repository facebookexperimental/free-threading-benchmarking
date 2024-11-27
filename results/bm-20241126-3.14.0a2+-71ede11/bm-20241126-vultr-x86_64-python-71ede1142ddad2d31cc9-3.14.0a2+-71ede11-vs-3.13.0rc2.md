# Results vs. 3.13.0rc2

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.006x slower
- HPT reliability: 96.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.01x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.63 sec: 1.01x slower                                                 |
| Geometric mean | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 409 ms: 1.13x faster                                                   |
| async_tree_none            | 354 ms                                                       | 333 ms: 1.06x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.4 ms: 1.05x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 879 ms: 1.04x faster                                                   |
| async_tree_io              | 876 ms                                                       | 855 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 664 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 225 ms: 1.04x slower                                                   |
| float          | 77.5 ms                                                      | 80.5 ms: 1.04x slower                                                  |
| nbody          | 85.1 ms                                                      | 95.1 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                  |
| regex_compile  | 132 ms                                                       | 135 ms: 1.02x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.0 us: 1.08x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 85.9 ms: 1.01x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 138 ms: 1.01x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 60.9 ms: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 218 us: 1.04x slower                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 98.9 ms: 1.04x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 320 us: 1.09x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.4 ms: 1.01x slower                                                  |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 22.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                   | 355 us                                                       | 261 us: 1.36x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                  |
| pylint                     | 317 ms                                                       | 270 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.66 us: 1.17x faster                                                  |
| go                         | 141 ms                                                       | 122 ms: 1.15x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 409 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                  |
| json_loads                 | 27.0 us                                                      | 25.0 us: 1.08x faster                                                  |
| json                       | 4.93 ms                                                      | 4.60 ms: 1.07x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.30 ms: 1.07x faster                                                  |
| async_tree_none            | 354 ms                                                       | 333 ms: 1.06x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.4 ms: 1.05x faster                                                  |
| thrift                     | 778 us                                                       | 743 us: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.7 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 879 ms: 1.04x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                                  |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                   |
| async_tree_io              | 876 ms                                                       | 855 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.02x faster                                                 |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                   |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 728 ms: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| 2to3                       | 260 ms                                                       | 258 ms: 1.01x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 67.7 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.01x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.63 sec: 1.01x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 85.9 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.4 ms: 1.01x slower                                                  |
| pyflate                    | 449 ms                                                       | 453 ms: 1.01x slower                                                   |
| fannkuch                   | 370 ms                                                       | 374 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 114 ms: 1.01x slower                                                   |
| xml_etree_parse            | 136 ms                                                       | 138 ms: 1.01x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 107 ms: 1.01x slower                                                   |
| sympy_expand               | 457 ms                                                       | 464 ms: 1.02x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.10 ms: 1.02x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 76.2 ms: 1.02x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 53.8 ms: 1.02x slower                                                  |
| regex_compile              | 132 ms                                                       | 135 ms: 1.02x slower                                                   |
| chaos                      | 57.3 ms                                                      | 58.6 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                   |
| logging_simple             | 6.16 us                                                      | 6.32 us: 1.03x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 60.9 ms: 1.03x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.06 us: 1.03x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 218 us: 1.04x slower                                                   |
| pidigits                   | 217 ms                                                       | 225 ms: 1.04x slower                                                   |
| float                      | 77.5 ms                                                      | 80.5 ms: 1.04x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 664 ms: 1.04x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 98.9 ms: 1.04x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| richards_super             | 51.6 ms                                                      | 54.1 ms: 1.05x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 22.6 ms: 1.05x slower                                                  |
| richards                   | 45.2 ms                                                      | 47.4 ms: 1.05x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.4 us: 1.06x slower                                                  |
| raytrace                   | 253 ms                                                       | 267 ms: 1.06x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.49 sec: 1.06x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.32 ms: 1.06x slower                                                  |
| logging_silent             | 103 ns                                                       | 110 ns: 1.07x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 320 us: 1.09x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                  |
| nbody                      | 85.1 ms                                                      | 95.1 ms: 1.12x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.95 ms: 1.26x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.95 ms: 1.46x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 86.4 ms: 7.86x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (10): async_tree_cpu_io_mixed, scimark_sor, scimark_sparse_mat_mult, bpe_tokeniser, sqlite_synth, sympy_str, regex_dna, scimark_monte_carlo, nqueens, async_tree_none_tg
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 96.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x