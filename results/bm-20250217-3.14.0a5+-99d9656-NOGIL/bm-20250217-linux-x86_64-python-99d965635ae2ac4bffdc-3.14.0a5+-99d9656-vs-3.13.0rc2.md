# Results vs. 3.13.0rc2

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.051x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 539 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 814 ms: 1.72x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 871 ms: 1.59x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 349 ms: 1.44x faster                                                   |
| async_tree_none            | 572 ms                                                       | 417 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 496 ms: 1.35x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 547 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 668 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 737 ms: 1.21x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmark hidden because not significant (3): async_generators, asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 104 ms: 1.11x faster                                                   |
| nbody          | 119 ms                                                       | 180 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 299 ms: 1.06x slower                                                   |
| regex_compile  | 182 ms                                                       | 199 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 139 ms: 1.27x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 210 ms: 1.10x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 130 ms: 1.06x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.05 sec: 1.10x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 95.8 ms: 1.12x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 483 us: 1.16x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.5 ms: 1.17x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 346 us: 1.19x slower                                                   |
| json_loads           | 34.3 us                                                      | 41.8 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.7 ms: 1.35x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.7 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 79.3 ms: 1.10x slower                                                  |
| django_template | 44.3 ms                                                      | 53.0 ms: 1.20x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 39.4 ms: 1.25x slower                                                  |
| mako            | 15.9 ms                                                      | 22.2 ms: 1.39x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 5.70 ms                                                      | 3.28 ms: 1.74x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 814 ms: 1.72x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 871 ms: 1.59x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 349 ms: 1.44x faster                                                   |
| async_tree_none            | 572 ms                                                       | 417 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 496 ms: 1.35x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 547 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 668 ms: 1.28x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 139 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 737 ms: 1.21x faster                                                   |
| deepcopy                   | 498 us                                                       | 417 us: 1.19x faster                                                   |
| spectral_norm              | 157 ms                                                       | 139 ms: 1.13x faster                                                   |
| float                      | 116 ms                                                       | 104 ms: 1.11x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 210 ms: 1.10x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.64 us: 1.10x faster                                                  |
| scimark_sor                | 179 ms                                                       | 168 ms: 1.06x faster                                                   |
| telco                      | 12.2 ms                                                      | 11.7 ms: 1.04x faster                                                  |
| go                         | 191 ms                                                       | 200 ms: 1.05x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 31.5 ms: 1.05x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 130 ms: 1.06x slower                                                   |
| richards                   | 65.5 ms                                                      | 69.4 ms: 1.06x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 1.66 sec: 1.06x slower                                                 |
| regex_dna                  | 282 ms                                                       | 299 ms: 1.06x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.07 sec: 1.07x slower                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 81.4 ms: 1.09x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 103 ms: 1.09x slower                                                   |
| regex_compile              | 182 ms                                                       | 199 ms: 1.10x slower                                                   |
| richards_super             | 73.2 ms                                                      | 80.2 ms: 1.10x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.05 sec: 1.10x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 79.3 ms: 1.10x slower                                                  |
| logging_silent             | 130 ns                                                       | 143 ns: 1.10x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 6.92 sec: 1.10x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 33.4 ms: 1.10x slower                                                  |
| sympy_str                  | 379 ms                                                       | 419 ms: 1.10x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.46 us: 1.11x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 95.8 ms: 1.12x slower                                                  |
| scimark_fft                | 473 ms                                                       | 531 ms: 1.12x slower                                                   |
| pyflate                    | 664 ms                                                       | 748 ms: 1.13x slower                                                   |
| chaos                      | 83.6 ms                                                      | 94.2 ms: 1.13x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.11 sec: 1.13x slower                                                 |
| generators                 | 40.0 ms                                                      | 45.3 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 159 ms: 1.13x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.27 ms: 1.15x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.7 us: 1.16x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 243 ms: 1.16x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 483 us: 1.16x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 16.5 ms: 1.17x slower                                                  |
| nqueens                    | 112 ms                                                       | 131 ms: 1.17x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.30 sec: 1.18x slower                                                 |
| meteor_contest             | 150 ms                                                       | 178 ms: 1.18x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.27 ms: 1.19x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 268 us: 1.19x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 346 us: 1.19x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 119 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.06 ms: 1.19x slower                                                  |
| django_template            | 44.3 ms                                                      | 53.0 ms: 1.20x slower                                                  |
| sympy_expand               | 601 ms                                                       | 722 ms: 1.20x slower                                                   |
| 2to3                       | 445 ms                                                       | 539 ms: 1.21x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.3 us: 1.22x slower                                                  |
| json_loads                 | 34.3 us                                                      | 41.8 us: 1.22x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 179 ms: 1.22x slower                                                   |
| json                       | 6.51 ms                                                      | 7.97 ms: 1.22x slower                                                  |
| fannkuch                   | 547 ms                                                       | 673 ms: 1.23x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 112 ms: 1.23x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 39.4 ms: 1.25x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.74 ms: 1.25x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 10.2 ms: 1.25x slower                                                  |
| raytrace                   | 344 ms                                                       | 441 ms: 1.28x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 2.25 ms: 1.28x slower                                                  |
| coverage                   | 107 ms                                                       | 140 ms: 1.31x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 20.7 ms: 1.35x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.94 ms: 1.36x slower                                                  |
| mako                       | 15.9 ms                                                      | 22.2 ms: 1.39x slower                                                  |
| python_startup             | 22.4 ms                                                      | 31.7 ms: 1.42x slower                                                  |
| nbody                      | 119 ms                                                       | 180 ms: 1.51x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 84.3 ms: 4.51x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (12): pidigits, pylint, regex_effbot, async_generators, asyncio_websockets, deepcopy_memo, create_gc_cycles, deepcopy_reduce, coroutines, docutils, regex_v8, html5lib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.051x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x