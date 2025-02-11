# Results vs. 3.13.0rc2

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.070x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 542 ms: 1.22x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.14 sec: 1.03x slower                                                 |
| html5lib       | 92.6 ms                                                      | 109 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 790 ms: 1.78x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 842 ms: 1.65x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 460 ms: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 399 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 363 ms: 1.39x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 540 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 654 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 766 ms: 1.16x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 231 ms: 1.09x faster                                                   |
| nbody          | 119 ms                                                       | 189 ms: 1.59x slower                                                   |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 269 ms: 1.05x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.52 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 203 ms: 1.14x faster                                                   |
| pickle_pure_python   | 416 us                                                       | 450 us: 1.08x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.03 sec: 1.09x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 96.3 ms: 1.12x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 140 ms: 1.15x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 361 us: 1.24x slower                                                   |
| json_loads           | 34.3 us                                                      | 42.9 us: 1.25x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 17.7 ms: 1.26x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.8 ms: 1.36x slower                                                  |
| python_startup         | 22.4 ms                                                      | 33.0 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 39.0 ms: 1.23x slower                                                  |
| django_template | 44.3 ms                                                      | 56.4 ms: 1.27x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 95.7 ms: 1.33x slower                                                  |
| mako            | 15.9 ms                                                      | 25.2 ms: 1.58x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.35x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 790 ms: 1.78x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 842 ms: 1.65x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 460 ms: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 399 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 363 ms: 1.39x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 540 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 654 ms: 1.30x faster                                                   |
| deepcopy                   | 498 us                                                       | 387 us: 1.29x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 4.44 ms: 1.28x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 766 ms: 1.16x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 203 ms: 1.14x faster                                                   |
| pidigits                   | 251 ms                                                       | 231 ms: 1.09x faster                                                   |
| regex_dna                  | 282 ms                                                       | 269 ms: 1.05x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.52 ms: 1.05x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| docutils                   | 4.01 sec                                                     | 4.14 sec: 1.03x slower                                                 |
| pycparser                  | 1.57 sec                                                     | 1.64 sec: 1.04x slower                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 79.3 ms: 1.06x slower                                                  |
| telco                      | 12.2 ms                                                      | 12.9 ms: 1.06x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 450 us: 1.08x slower                                                   |
| pyflate                    | 664 ms                                                       | 722 ms: 1.09x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.03 sec: 1.09x slower                                                 |
| logging_silent             | 130 ns                                                       | 142 ns: 1.09x slower                                                   |
| sympy_expand               | 601 ms                                                       | 663 ms: 1.10x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.20 sec: 1.10x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.56 us: 1.11x slower                                                  |
| richards                   | 65.5 ms                                                      | 73.2 ms: 1.12x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 96.3 ms: 1.12x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 157 ms: 1.12x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 236 ms: 1.13x slower                                                   |
| json                       | 6.51 ms                                                      | 7.34 ms: 1.13x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 106 ms: 1.13x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 140 ms: 1.15x slower                                                   |
| comprehensions             | 22.2 us                                                      | 25.5 us: 1.15x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 34.7 ms: 1.15x slower                                                  |
| fannkuch                   | 547 ms                                                       | 630 ms: 1.15x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.14 sec: 1.15x slower                                                 |
| scimark_fft                | 473 ms                                                       | 547 ms: 1.16x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.27 ms: 1.16x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 109 ms: 1.18x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.29 sec: 1.18x slower                                                 |
| logging_simple             | 8.56 us                                                      | 10.1 us: 1.18x slower                                                  |
| richards_super             | 73.2 ms                                                      | 86.5 ms: 1.18x slower                                                  |
| chaos                      | 83.6 ms                                                      | 99.1 ms: 1.19x slower                                                  |
| meteor_contest             | 150 ms                                                       | 179 ms: 1.19x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 120 ms: 1.19x slower                                                   |
| nqueens                    | 112 ms                                                       | 133 ms: 1.19x slower                                                   |
| sympy_str                  | 379 ms                                                       | 454 ms: 1.20x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.60 sec: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.18 ms: 1.21x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 9.84 ms: 1.21x slower                                                  |
| 2to3                       | 445 ms                                                       | 542 ms: 1.22x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 179 ms: 1.23x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 39.0 ms: 1.23x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.17 ms: 1.24x slower                                                  |
| generators                 | 40.0 ms                                                      | 49.5 ms: 1.24x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 361 us: 1.24x slower                                                   |
| json_loads                 | 34.3 us                                                      | 42.9 us: 1.25x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.7 ms: 1.26x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.76 ms: 1.26x slower                                                  |
| raytrace                   | 344 ms                                                       | 437 ms: 1.27x slower                                                   |
| django_template            | 44.3 ms                                                      | 56.4 ms: 1.27x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 289 us: 1.28x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.9 us: 1.28x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.11 ms: 1.29x slower                                                  |
| coverage                   | 107 ms                                                       | 140 ms: 1.30x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 95.7 ms: 1.33x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.89 ms: 1.35x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 20.8 ms: 1.36x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 124 ms: 1.37x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 6.45 ms: 1.45x slower                                                  |
| python_startup             | 22.4 ms                                                      | 33.0 ms: 1.47x slower                                                  |
| mako                       | 15.9 ms                                                      | 25.2 ms: 1.58x slower                                                  |
| nbody                      | 119 ms                                                       | 189 ms: 1.59x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 87.5 ms: 4.68x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (12): scimark_sor, float, go, async_generators, pylint, spectral_norm, sqlite_synth, regex_v8, deepcopy_memo, pathlib, regex_compile, coroutines
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.070x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x