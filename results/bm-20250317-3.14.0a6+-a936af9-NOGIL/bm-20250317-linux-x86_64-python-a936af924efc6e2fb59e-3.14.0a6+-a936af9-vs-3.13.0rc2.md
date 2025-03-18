# Results vs. 3.13.0rc2

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.055x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 540 ms: 1.21x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.13 sec: 1.03x slower                                                 |
| html5lib       | 92.6 ms                                                      | 98.0 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 733 ms: 1.91x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 812 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 314 ms: 1.60x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 454 ms: 1.48x faster                                                   |
| async_tree_none            | 572 ms                                                       | 390 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 501 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 681 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 732 ms: 1.21x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 727 ms: 1.05x faster                                                   |
| async_generators           | 567 ms                                                       | 590 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 172 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.25 ms: 1.12x faster                                                  |
| regex_dna      | 282 ms                                                       | 304 ms: 1.08x slower                                                   |
| regex_compile  | 182 ms                                                       | 212 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 140 ms: 1.26x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 206 ms: 1.12x faster                                                   |
| xml_etree_process    | 85.9 ms                                                      | 92.3 ms: 1.07x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 321 us: 1.11x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.09 sec: 1.11x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 145 ms: 1.18x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 523 us: 1.25x slower                                                   |
| json_loads           | 34.3 us                                                      | 47.8 us: 1.39x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 34.9 ms: 1.56x slower                                                  |
| python_startup_no_site | 15.3 ms                                                      | 25.6 ms: 1.67x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.61x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 87.3 ms: 1.21x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 39.5 ms: 1.25x slower                                                  |
| django_template | 44.3 ms                                                      | 55.3 ms: 1.25x slower                                                  |
| mako            | 15.9 ms                                                      | 25.0 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 733 ms: 1.91x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 812 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 314 ms: 1.60x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 454 ms: 1.48x faster                                                   |
| async_tree_none            | 572 ms                                                       | 390 ms: 1.47x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.97 ms: 1.43x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 501 ms: 1.42x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 140 ms: 1.26x faster                                                   |
| deepcopy                   | 498 us                                                       | 395 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 681 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 732 ms: 1.21x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 206 ms: 1.12x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.57 us: 1.12x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.25 ms: 1.12x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 87.7 ms: 1.07x faster                                                  |
| spectral_norm              | 157 ms                                                       | 147 ms: 1.07x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 727 ms: 1.05x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 48.4 us: 1.04x faster                                                  |
| docutils                   | 4.01 sec                                                     | 4.13 sec: 1.03x slower                                                 |
| async_generators           | 567 ms                                                       | 590 ms: 1.04x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 31.4 ms: 1.05x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 98.0 ms: 1.06x slower                                                  |
| richards                   | 65.5 ms                                                      | 70.1 ms: 1.07x slower                                                  |
| pyflate                    | 664 ms                                                       | 711 ms: 1.07x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 92.3 ms: 1.07x slower                                                  |
| regex_dna                  | 282 ms                                                       | 304 ms: 1.08x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 82.4 ms: 1.10x slower                                                  |
| generators                 | 40.0 ms                                                      | 44.2 ms: 1.11x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 321 us: 1.11x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.09 sec: 1.11x slower                                                 |
| mdp                        | 3.80 sec                                                     | 4.22 sec: 1.11x slower                                                 |
| sqlglot_normalize          | 140 ms                                                       | 156 ms: 1.12x slower                                                   |
| scimark_fft                | 473 ms                                                       | 533 ms: 1.13x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 34.0 ms: 1.13x slower                                                  |
| chaos                      | 83.6 ms                                                      | 94.2 ms: 1.13x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.72 ms: 1.13x slower                                                  |
| json                       | 6.51 ms                                                      | 7.34 ms: 1.13x slower                                                  |
| sympy_str                  | 379 ms                                                       | 429 ms: 1.13x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.12 sec: 1.14x slower                                                 |
| crypto_pyaes               | 100 ms                                                       | 114 ms: 1.14x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.08 ms: 1.14x slower                                                  |
| fannkuch                   | 547 ms                                                       | 631 ms: 1.15x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.27 ms: 1.15x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.7 us: 1.15x slower                                                  |
| meteor_contest             | 150 ms                                                       | 174 ms: 1.16x slower                                                   |
| sympy_expand               | 601 ms                                                       | 696 ms: 1.16x slower                                                   |
| nqueens                    | 112 ms                                                       | 130 ms: 1.16x slower                                                   |
| regex_compile              | 182 ms                                                       | 212 ms: 1.17x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.38 sec: 1.17x slower                                                 |
| richards_super             | 73.2 ms                                                      | 86.4 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.29 sec: 1.18x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 107 ms: 1.18x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 145 ms: 1.18x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 251 ms: 1.19x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.62 ms: 1.19x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.1 us: 1.20x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 87.3 ms: 1.21x slower                                                  |
| 2to3                       | 445 ms                                                       | 540 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 275 us: 1.22x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.25 ms: 1.22x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 9.98 ms: 1.23x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 39.5 ms: 1.25x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 183 ms: 1.25x slower                                                   |
| django_template            | 44.3 ms                                                      | 55.3 ms: 1.25x slower                                                  |
| raytrace                   | 344 ms                                                       | 430 ms: 1.25x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 523 us: 1.25x slower                                                   |
| logging_simple             | 8.56 us                                                      | 11.0 us: 1.28x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.30 ms: 1.31x slower                                                  |
| coverage                   | 107 ms                                                       | 141 ms: 1.31x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.85 ms: 1.33x slower                                                  |
| json_loads                 | 34.3 us                                                      | 47.8 us: 1.39x slower                                                  |
| nbody                      | 119 ms                                                       | 172 ms: 1.45x slower                                                   |
| python_startup             | 22.4 ms                                                      | 34.9 ms: 1.56x slower                                                  |
| mako                       | 15.9 ms                                                      | 25.0 ms: 1.57x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 25.6 ms: 1.67x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 84.8 ms: 4.54x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (11): pylint, pidigits, coroutines, regex_v8, scimark_sor, deepcopy_reduce, float, pycparser, telco, go, logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.055x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x