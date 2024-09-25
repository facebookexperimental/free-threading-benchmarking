# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 690 ms: 1.51x slower                                  |
| docutils       | 4.05 sec                                             | 5.03 sec: 1.24x slower                                |
| html5lib       | 100 ms                                               | 138 ms: 1.37x slower                                  |
| tornado_http   | 261 ms                                               | 358 ms: 1.37x slower                                  |
| Geometric mean | (ref)                                                | 1.37x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.19 sec: 1.56x faster                                |
| async_tree_none_tg         | 726 ms                                               | 471 ms: 1.54x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.28 sec: 1.45x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 641 ms: 1.42x faster                                  |
| async_tree_none            | 820 ms                                               | 600 ms: 1.37x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 843 ms: 1.33x faster                                  |
| async_tree_memoization     | 975 ms                                               | 744 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 975 ms: 1.17x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.10 sec: 1.11x slower                                |
| async_generators           | 615 ms                                               | 741 ms: 1.21x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.42 sec: 1.21x slower                                |
| coroutines                 | 30.6 ms                                              | 42.7 ms: 1.40x slower                                 |
| Geometric mean             | (ref)                                                | 1.15x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 246 ms: 1.04x faster                                  |
| float          | 124 ms                                               | 201 ms: 1.62x slower                                  |
| nbody          | 117 ms                                               | 291 ms: 2.49x slower                                  |
| Geometric mean | (ref)                                                | 1.57x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.78 ms: 1.05x faster                                 |
| regex_dna      | 268 ms                                               | 289 ms: 1.08x slower                                  |
| regex_v8       | 29.9 ms                                              | 36.8 ms: 1.23x slower                                 |
| regex_compile  | 186 ms                                               | 292 ms: 1.57x slower                                  |
| Geometric mean | (ref)                                                | 1.19x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 213 ms: 1.14x faster                                  |
| pickle               | 15.9 us                                              | 14.4 us: 1.10x faster                                 |
| pickle_list          | 7.01 us                                              | 6.46 us: 1.09x faster                                 |
| xml_etree_generate   | 138 ms                                               | 163 ms: 1.18x slower                                  |
| json_loads           | 35.9 us                                              | 44.5 us: 1.24x slower                                 |
| json_dumps           | 14.0 ms                                              | 18.3 ms: 1.31x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.33 sec: 1.51x slower                                |
| xml_etree_process    | 82.7 ms                                              | 137 ms: 1.66x slower                                  |
| pickle_pure_python   | 436 us                                               | 768 us: 1.76x slower                                  |
| unpickle_pure_python | 304 us                                               | 573 us: 1.89x slower                                  |
| Geometric mean       | (ref)                                                | 1.19x slower                                          |

Benchmark hidden because not significant (4): pickle_dict, unpickle_list, unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 19.9 ms: 1.23x slower                                 |
| python_startup         | 22.7 ms                                              | 29.3 ms: 1.29x slower                                 |
| Geometric mean         | (ref)                                                | 1.26x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 117 ms: 1.69x slower                                  |
| django_template | 45.4 ms                                              | 81.6 ms: 1.80x slower                                 |
| mako            | 16.1 ms                                              | 29.5 ms: 1.83x slower                                 |
| genshi_text     | 30.3 ms                                              | 57.9 ms: 1.91x slower                                 |
| Geometric mean  | (ref)                                                | 1.81x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.19 sec: 1.56x faster                                |
| async_tree_none_tg         | 726 ms                                               | 471 ms: 1.54x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.28 sec: 1.45x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 641 ms: 1.42x faster                                  |
| gc_traversal               | 6.42 ms                                              | 4.66 ms: 1.38x faster                                 |
| async_tree_none            | 820 ms                                               | 600 ms: 1.37x faster                                  |
| bench_mp_pool              | 21.2 ms                                              | 15.8 ms: 1.35x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 843 ms: 1.33x faster                                  |
| async_tree_memoization     | 975 ms                                               | 744 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 975 ms: 1.17x faster                                  |
| xml_etree_parse            | 244 ms                                               | 213 ms: 1.14x faster                                  |
| pickle                     | 15.9 us                                              | 14.4 us: 1.10x faster                                 |
| pickle_list                | 7.01 us                                              | 6.46 us: 1.09x faster                                 |
| create_gc_cycles           | 2.00 ms                                              | 1.87 ms: 1.07x faster                                 |
| regex_effbot               | 5.02 ms                                              | 4.78 ms: 1.05x faster                                 |
| pidigits                   | 256 ms                                               | 246 ms: 1.04x faster                                  |
| regex_dna                  | 268 ms                                               | 289 ms: 1.08x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.10 sec: 1.11x slower                                |
| sqlite_synth               | 3.77 us                                              | 4.23 us: 1.12x slower                                 |
| pathlib                    | 31.6 ms                                              | 35.5 ms: 1.12x slower                                 |
| bench_thread_pool          | 3.42 ms                                              | 3.97 ms: 1.16x slower                                 |
| deepcopy                   | 486 us                                               | 566 us: 1.16x slower                                  |
| xml_etree_generate         | 138 ms                                               | 163 ms: 1.18x slower                                  |
| json                       | 7.14 ms                                              | 8.50 ms: 1.19x slower                                 |
| async_generators           | 615 ms                                               | 741 ms: 1.21x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.42 sec: 1.21x slower                                |
| python_startup_no_site     | 16.2 ms                                              | 19.9 ms: 1.23x slower                                 |
| regex_v8                   | 29.9 ms                                              | 36.8 ms: 1.23x slower                                 |
| json_loads                 | 35.9 us                                              | 44.5 us: 1.24x slower                                 |
| pylint                     | 480 ms                                               | 595 ms: 1.24x slower                                  |
| docutils                   | 4.05 sec                                             | 5.03 sec: 1.24x slower                                |
| generators                 | 44.7 ms                                              | 57.4 ms: 1.28x slower                                 |
| scimark_fft                | 481 ms                                               | 621 ms: 1.29x slower                                  |
| python_startup             | 22.7 ms                                              | 29.3 ms: 1.29x slower                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.05 ms: 1.30x slower                                 |
| nqueens                    | 116 ms                                               | 151 ms: 1.31x slower                                  |
| json_dumps                 | 14.0 ms                                              | 18.3 ms: 1.31x slower                                 |
| pycparser                  | 1.68 sec                                             | 2.21 sec: 1.32x slower                                |
| deepcopy_memo              | 51.0 us                                              | 67.8 us: 1.33x slower                                 |
| mdp                        | 3.77 sec                                             | 5.12 sec: 1.36x slower                                |
| crypto_pyaes               | 110 ms                                               | 149 ms: 1.36x slower                                  |
| comprehensions             | 28.6 us                                              | 39.2 us: 1.37x slower                                 |
| tornado_http               | 261 ms                                               | 358 ms: 1.37x slower                                  |
| html5lib                   | 100 ms                                               | 138 ms: 1.37x slower                                  |
| coroutines                 | 30.6 ms                                              | 42.7 ms: 1.40x slower                                 |
| meteor_contest             | 146 ms                                               | 206 ms: 1.41x slower                                  |
| deepcopy_reduce            | 4.18 us                                              | 6.02 us: 1.44x slower                                 |
| telco                      | 9.53 ms                                              | 13.8 ms: 1.45x slower                                 |
| bpe_tokeniser              | 6.76 sec                                             | 9.93 sec: 1.47x slower                                |
| tomli_loads                | 2.86 sec                                             | 4.33 sec: 1.51x slower                                |
| 2to3                       | 456 ms                                               | 690 ms: 1.51x slower                                  |
| sympy_integrate            | 29.0 ms                                              | 44.3 ms: 1.53x slower                                 |
| fannkuch                   | 525 ms                                               | 802 ms: 1.53x slower                                  |
| sqlglot_optimize           | 80.2 ms                                              | 123 ms: 1.53x slower                                  |
| coverage                   | 96.9 ms                                              | 149 ms: 1.54x slower                                  |
| regex_compile              | 186 ms                                               | 292 ms: 1.57x slower                                  |
| thrift                     | 1.10 ms                                              | 1.77 ms: 1.60x slower                                 |
| float                      | 124 ms                                               | 201 ms: 1.62x slower                                  |
| sqlglot_normalize          | 144 ms                                               | 233 ms: 1.63x slower                                  |
| logging_simple             | 9.68 us                                              | 15.9 us: 1.64x slower                                 |
| pyflate                    | 664 ms                                               | 1.09 sec: 1.65x slower                                |
| xml_etree_process          | 82.7 ms                                              | 137 ms: 1.66x slower                                  |
| richards                   | 62.8 ms                                              | 105 ms: 1.66x slower                                  |
| typing_runtime_protocols   | 224 us                                               | 377 us: 1.68x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 117 ms: 1.69x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 168 ms: 1.74x slower                                  |
| pickle_pure_python         | 436 us                                               | 768 us: 1.76x slower                                  |
| spectral_norm              | 136 ms                                               | 244 ms: 1.79x slower                                  |
| pprint_safe_repr           | 972 ms                                               | 1.74 sec: 1.79x slower                                |
| django_template            | 45.4 ms                                              | 81.6 ms: 1.80x slower                                 |
| pprint_pformat             | 1.99 sec                                             | 3.60 sec: 1.82x slower                                |
| mako                       | 16.1 ms                                              | 29.5 ms: 1.83x slower                                 |
| logging_silent             | 139 ns                                               | 259 ns: 1.86x slower                                  |
| sympy_str                  | 379 ms                                               | 713 ms: 1.88x slower                                  |
| unpickle_pure_python       | 304 us                                               | 573 us: 1.89x slower                                  |
| chaos                      | 92.1 ms                                              | 175 ms: 1.90x slower                                  |
| logging_format             | 9.56 us                                              | 18.2 us: 1.91x slower                                 |
| genshi_text                | 30.3 ms                                              | 57.9 ms: 1.91x slower                                 |
| richards_super             | 69.7 ms                                              | 134 ms: 1.92x slower                                  |
| raytrace                   | 405 ms                                               | 805 ms: 1.99x slower                                  |
| hexiom                     | 8.19 ms                                              | 16.3 ms: 2.00x slower                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.65 ms: 2.00x slower                                 |
| scimark_sor                | 170 ms                                               | 342 ms: 2.01x slower                                  |
| sqlglot_parse              | 1.85 ms                                              | 3.81 ms: 2.06x slower                                 |
| scimark_lu                 | 155 ms                                               | 323 ms: 2.08x slower                                  |
| sympy_expand               | 591 ms                                               | 1.29 sec: 2.19x slower                                |
| sympy_sum                  | 218 ms                                               | 487 ms: 2.24x slower                                  |
| go                         | 173 ms                                               | 405 ms: 2.34x slower                                  |
| nbody                      | 117 ms                                               | 291 ms: 2.49x slower                                  |
| unpack_sequence            | 70.8 ns                                              | 190 ns: 2.69x slower                                  |
| deltablue                  | 4.45 ms                                              | 12.1 ms: 2.72x slower                                 |
| Geometric mean             | (ref)                                                | 1.36x slower                                          |

Benchmark hidden because not significant (5): pickle_dict, unpickle_list, asyncio_websockets, unpickle, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.16x