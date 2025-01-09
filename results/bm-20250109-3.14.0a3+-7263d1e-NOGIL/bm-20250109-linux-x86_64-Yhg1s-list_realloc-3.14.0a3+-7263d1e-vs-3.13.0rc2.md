# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: list_realloc
- machine: linux-x86_64
- commit hash: 7263d1e
- commit date: 2025-01-09
- overall geometric mean: 1.206x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 653 ms: 1.47x slower                                          |
| docutils       | 4.01 sec                                                     | 4.77 sec: 1.19x slower                                        |
| html5lib       | 92.6 ms                                                      | 121 ms: 1.31x slower                                          |
| Geometric mean | (ref)                                                        | 1.32x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 984 ms: 1.42x faster                                          |
| async_tree_io              | 1.39 sec                                                     | 1.05 sec: 1.32x faster                                        |
| async_tree_memoization     | 709 ms                                                       | 598 ms: 1.19x faster                                          |
| async_tree_none_tg         | 504 ms                                                       | 439 ms: 1.15x faster                                          |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 752 ms: 1.13x faster                                          |
| async_tree_none            | 572 ms                                                       | 512 ms: 1.12x faster                                          |
| async_tree_memoization_tg  | 670 ms                                                       | 601 ms: 1.12x faster                                          |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 844 ms: 1.05x faster                                          |
| coroutines                 | 30.9 ms                                                      | 36.1 ms: 1.17x slower                                         |
| async_generators           | 567 ms                                                       | 674 ms: 1.19x slower                                          |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                  |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 116 ms                                                       | 143 ms: 1.24x slower                                          |
| nbody          | 119 ms                                                       | 179 ms: 1.51x slower                                          |
| Geometric mean | (ref)                                                        | 1.25x slower                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.34 ms: 1.09x faster                                         |
| regex_dna      | 282 ms                                                       | 327 ms: 1.16x slower                                          |
| regex_v8       | 32.8 ms                                                      | 41.0 ms: 1.25x slower                                         |
| regex_compile  | 182 ms                                                       | 228 ms: 1.25x slower                                          |
| Geometric mean | (ref)                                                        | 1.14x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_generate   | 122 ms                                                       | 142 ms: 1.16x slower                                          |
| json_loads           | 34.3 us                                                      | 40.0 us: 1.17x slower                                         |
| tomli_loads          | 2.78 sec                                                     | 3.25 sec: 1.17x slower                                        |
| xml_etree_process    | 85.9 ms                                                      | 101 ms: 1.17x slower                                          |
| json_dumps           | 14.1 ms                                                      | 16.7 ms: 1.18x slower                                         |
| unpickle_pure_python | 290 us                                                       | 410 us: 1.41x slower                                          |
| pickle_pure_python   | 416 us                                                       | 661 us: 1.59x slower                                          |
| Geometric mean       | (ref)                                                        | 1.18x slower                                                  |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 23.8 ms: 1.56x slower                                         |
| python_startup         | 22.4 ms                                                      | 38.1 ms: 1.70x slower                                         |
| Geometric mean         | (ref)                                                        | 1.63x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 89.0 ms: 1.23x slower                                         |
| genshi_text     | 31.7 ms                                                      | 39.5 ms: 1.25x slower                                         |
| django_template | 44.3 ms                                                      | 67.0 ms: 1.51x slower                                         |
| mako            | 15.9 ms                                                      | 30.4 ms: 1.90x slower                                         |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 984 ms: 1.42x faster                                          |
| async_tree_io              | 1.39 sec                                                     | 1.05 sec: 1.32x faster                                        |
| async_tree_memoization     | 709 ms                                                       | 598 ms: 1.19x faster                                          |
| async_tree_none_tg         | 504 ms                                                       | 439 ms: 1.15x faster                                          |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 752 ms: 1.13x faster                                          |
| async_tree_none            | 572 ms                                                       | 512 ms: 1.12x faster                                          |
| async_tree_memoization_tg  | 670 ms                                                       | 601 ms: 1.12x faster                                          |
| deepcopy                   | 498 us                                                       | 454 us: 1.10x faster                                          |
| regex_effbot               | 4.74 ms                                                      | 4.34 ms: 1.09x faster                                         |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 844 ms: 1.05x faster                                          |
| spectral_norm              | 157 ms                                                       | 167 ms: 1.06x slower                                          |
| pycparser                  | 1.57 sec                                                     | 1.74 sec: 1.11x slower                                        |
| deepcopy_memo              | 50.1 us                                                      | 56.3 us: 1.12x slower                                         |
| json                       | 6.51 ms                                                      | 7.37 ms: 1.13x slower                                         |
| sqlglot_optimize           | 74.7 ms                                                      | 85.3 ms: 1.14x slower                                         |
| pathlib                    | 29.9 ms                                                      | 34.4 ms: 1.15x slower                                         |
| sympy_str                  | 379 ms                                                       | 436 ms: 1.15x slower                                          |
| regex_dna                  | 282 ms                                                       | 327 ms: 1.16x slower                                          |
| telco                      | 12.2 ms                                                      | 14.1 ms: 1.16x slower                                         |
| xml_etree_generate         | 122 ms                                                       | 142 ms: 1.16x slower                                          |
| json_loads                 | 34.3 us                                                      | 40.0 us: 1.17x slower                                         |
| deepcopy_reduce            | 4.10 us                                                      | 4.79 us: 1.17x slower                                         |
| tomli_loads                | 2.78 sec                                                     | 3.25 sec: 1.17x slower                                        |
| coroutines                 | 30.9 ms                                                      | 36.1 ms: 1.17x slower                                         |
| xml_etree_process          | 85.9 ms                                                      | 101 ms: 1.17x slower                                          |
| json_dumps                 | 14.1 ms                                                      | 16.7 ms: 1.18x slower                                         |
| async_generators           | 567 ms                                                       | 674 ms: 1.19x slower                                          |
| docutils                   | 4.01 sec                                                     | 4.77 sec: 1.19x slower                                        |
| pylint                     | 470 ms                                                       | 570 ms: 1.21x slower                                          |
| coverage                   | 107 ms                                                       | 130 ms: 1.21x slower                                          |
| sympy_expand               | 601 ms                                                       | 736 ms: 1.23x slower                                          |
| scimark_fft                | 473 ms                                                       | 583 ms: 1.23x slower                                          |
| genshi_xml                 | 72.1 ms                                                      | 89.0 ms: 1.23x slower                                         |
| float                      | 116 ms                                                       | 143 ms: 1.24x slower                                          |
| genshi_text                | 31.7 ms                                                      | 39.5 ms: 1.25x slower                                         |
| regex_v8                   | 32.8 ms                                                      | 41.0 ms: 1.25x slower                                         |
| regex_compile              | 182 ms                                                       | 228 ms: 1.25x slower                                          |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.50 ms: 1.26x slower                                         |
| dulwich_log                | 93.7 ms                                                      | 119 ms: 1.27x slower                                          |
| crypto_pyaes               | 100 ms                                                       | 128 ms: 1.28x slower                                          |
| richards                   | 65.5 ms                                                      | 84.0 ms: 1.28x slower                                         |
| meteor_contest             | 150 ms                                                       | 193 ms: 1.28x slower                                          |
| nqueens                    | 112 ms                                                       | 145 ms: 1.30x slower                                          |
| sqlglot_normalize          | 140 ms                                                       | 182 ms: 1.30x slower                                          |
| html5lib                   | 92.6 ms                                                      | 121 ms: 1.31x slower                                          |
| pprint_safe_repr           | 987 ms                                                       | 1.30 sec: 1.32x slower                                        |
| typing_runtime_protocols   | 226 us                                                       | 301 us: 1.33x slower                                          |
| mdp                        | 3.80 sec                                                     | 5.15 sec: 1.36x slower                                        |
| bpe_tokeniser              | 6.28 sec                                                     | 8.65 sec: 1.38x slower                                        |
| sympy_sum                  | 210 ms                                                       | 290 ms: 1.38x slower                                          |
| scimark_sor                | 179 ms                                                       | 250 ms: 1.40x slower                                          |
| scimark_lu                 | 146 ms                                                       | 205 ms: 1.40x slower                                          |
| unpickle_pure_python       | 290 us                                                       | 410 us: 1.41x slower                                          |
| richards_super             | 73.2 ms                                                      | 103 ms: 1.41x slower                                          |
| scimark_monte_carlo        | 90.6 ms                                                      | 129 ms: 1.42x slower                                          |
| generators                 | 40.0 ms                                                      | 56.9 ms: 1.42x slower                                         |
| pprint_pformat             | 1.94 sec                                                     | 2.80 sec: 1.44x slower                                        |
| thrift                     | 1.10 ms                                                      | 1.59 ms: 1.44x slower                                         |
| pyflate                    | 664 ms                                                       | 962 ms: 1.45x slower                                          |
| 2to3                       | 445 ms                                                       | 653 ms: 1.47x slower                                          |
| sympy_integrate            | 30.2 ms                                                      | 44.7 ms: 1.48x slower                                         |
| go                         | 191 ms                                                       | 287 ms: 1.50x slower                                          |
| nbody                      | 119 ms                                                       | 179 ms: 1.51x slower                                          |
| fannkuch                   | 547 ms                                                       | 826 ms: 1.51x slower                                          |
| django_template            | 44.3 ms                                                      | 67.0 ms: 1.51x slower                                         |
| python_startup_no_site     | 15.3 ms                                                      | 23.8 ms: 1.56x slower                                         |
| hexiom                     | 8.11 ms                                                      | 12.7 ms: 1.57x slower                                         |
| pickle_pure_python         | 416 us                                                       | 661 us: 1.59x slower                                          |
| logging_simple             | 8.56 us                                                      | 13.7 us: 1.60x slower                                         |
| gc_traversal               | 5.70 ms                                                      | 9.15 ms: 1.61x slower                                         |
| chaos                      | 83.6 ms                                                      | 135 ms: 1.61x slower                                          |
| logging_format             | 9.24 us                                                      | 15.4 us: 1.67x slower                                         |
| comprehensions             | 22.2 us                                                      | 37.2 us: 1.67x slower                                         |
| python_startup             | 22.4 ms                                                      | 38.1 ms: 1.70x slower                                         |
| sqlglot_transpile          | 2.20 ms                                                      | 3.97 ms: 1.81x slower                                         |
| sqlglot_parse              | 1.76 ms                                                      | 3.25 ms: 1.85x slower                                         |
| bench_thread_pool          | 2.89 ms                                                      | 5.37 ms: 1.86x slower                                         |
| raytrace                   | 344 ms                                                       | 641 ms: 1.86x slower                                          |
| logging_silent             | 130 ns                                                       | 244 ns: 1.87x slower                                          |
| mako                       | 15.9 ms                                                      | 30.4 ms: 1.90x slower                                         |
| deltablue                  | 4.44 ms                                                      | 9.95 ms: 2.24x slower                                         |
| create_gc_cycles           | 2.41 ms                                                      | 6.43 ms: 2.67x slower                                         |
| bench_mp_pool              | 18.7 ms                                                      | 111 ms: 5.93x slower                                          |
| Geometric mean             | (ref)                                                        | 1.31x slower                                                  |

Benchmark hidden because not significant (5): xml_etree_iterparse, xml_etree_parse, sqlite_synth, asyncio_websockets, pidigits
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250109-3.14.0a3+-7263d1e-NOGIL/bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.206x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x