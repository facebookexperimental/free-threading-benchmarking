# Results vs. 3.12.5+

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.34x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 647 ms: 1.42x slower                                                  |
| docutils       | 4.05 sec                                             | 4.82 sec: 1.19x slower                                                |
| html5lib       | 100 ms                                               | 141 ms: 1.41x slower                                                  |
| tornado_http   | 261 ms                                               | 342 ms: 1.31x slower                                                  |
| Geometric mean | (ref)                                                | 1.33x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.12 sec: 1.67x faster                                                |
| async_tree_io              | 1.86 sec                                             | 1.23 sec: 1.51x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 482 ms: 1.51x faster                                                  |
| async_tree_none            | 820 ms                                               | 566 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 632 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 820 ms: 1.37x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 721 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 913 ms: 1.25x faster                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.18 sec: 1.13x slower                                                |
| async_generators           | 615 ms                                               | 723 ms: 1.18x slower                                                  |
| coroutines                 | 30.6 ms                                              | 39.3 ms: 1.28x slower                                                 |
| Geometric mean             | (ref)                                                | 1.20x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                               | 242 ms: 1.06x faster                                                  |
| float          | 124 ms                                               | 193 ms: 1.55x slower                                                  |
| nbody          | 117 ms                                               | 280 ms: 2.40x slower                                                  |
| Geometric mean | (ref)                                                | 1.52x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.47 ms: 1.12x faster                                                 |
| regex_dna      | 268 ms                                               | 295 ms: 1.10x slower                                                  |
| regex_v8       | 29.9 ms                                              | 35.3 ms: 1.18x slower                                                 |
| regex_compile  | 186 ms                                               | 293 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                | 1.16x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 201 ms: 1.21x faster                                                  |
| pickle               | 15.9 us                                              | 14.5 us: 1.09x faster                                                 |
| xml_etree_iterparse  | 173 ms                                               | 159 ms: 1.09x faster                                                  |
| pickle_list          | 7.01 us                                              | 6.53 us: 1.07x faster                                                 |
| pickle_dict          | 45.5 us                                              | 44.0 us: 1.03x faster                                                 |
| unpickle_list        | 6.83 us                                              | 7.76 us: 1.14x slower                                                 |
| xml_etree_generate   | 138 ms                                               | 160 ms: 1.17x slower                                                  |
| json_loads           | 35.9 us                                              | 43.6 us: 1.21x slower                                                 |
| json_dumps           | 14.0 ms                                              | 17.8 ms: 1.27x slower                                                 |
| tomli_loads          | 2.86 sec                                             | 4.22 sec: 1.48x slower                                                |
| xml_etree_process    | 82.7 ms                                              | 126 ms: 1.53x slower                                                  |
| unpickle_pure_python | 304 us                                               | 558 us: 1.84x slower                                                  |
| pickle_pure_python   | 436 us                                               | 830 us: 1.90x slower                                                  |
| Geometric mean       | (ref)                                                | 1.18x slower                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 19.5 ms: 1.20x slower                                                 |
| python_startup         | 22.7 ms                                              | 28.9 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 120 ms: 1.73x slower                                                  |
| django_template | 45.4 ms                                              | 80.6 ms: 1.78x slower                                                 |
| genshi_text     | 30.3 ms                                              | 54.4 ms: 1.79x slower                                                 |
| mako            | 16.1 ms                                              | 29.9 ms: 1.85x slower                                                 |
| Geometric mean  | (ref)                                                | 1.79x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.12 sec: 1.67x faster                                                |
| bench_mp_pool              | 21.2 ms                                              | 13.6 ms: 1.56x faster                                                 |
| async_tree_io              | 1.86 sec                                             | 1.23 sec: 1.51x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 482 ms: 1.51x faster                                                  |
| gc_traversal               | 6.42 ms                                              | 4.28 ms: 1.50x faster                                                 |
| async_tree_none            | 820 ms                                               | 566 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 632 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 820 ms: 1.37x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 721 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 913 ms: 1.25x faster                                                  |
| xml_etree_parse            | 244 ms                                               | 201 ms: 1.21x faster                                                  |
| regex_effbot               | 5.02 ms                                              | 4.47 ms: 1.12x faster                                                 |
| pickle                     | 15.9 us                                              | 14.5 us: 1.09x faster                                                 |
| xml_etree_iterparse        | 173 ms                                               | 159 ms: 1.09x faster                                                  |
| pickle_list                | 7.01 us                                              | 6.53 us: 1.07x faster                                                 |
| pidigits                   | 256 ms                                               | 242 ms: 1.06x faster                                                  |
| pickle_dict                | 45.5 us                                              | 44.0 us: 1.03x faster                                                 |
| json                       | 7.14 ms                                              | 7.69 ms: 1.08x slower                                                 |
| regex_dna                  | 268 ms                                               | 295 ms: 1.10x slower                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.18 sec: 1.13x slower                                                |
| sqlite_synth               | 3.77 us                                              | 4.28 us: 1.13x slower                                                 |
| unpickle_list              | 6.83 us                                              | 7.76 us: 1.14x slower                                                 |
| xml_etree_generate         | 138 ms                                               | 160 ms: 1.17x slower                                                  |
| pylint                     | 480 ms                                               | 562 ms: 1.17x slower                                                  |
| async_generators           | 615 ms                                               | 723 ms: 1.18x slower                                                  |
| regex_v8                   | 29.9 ms                                              | 35.3 ms: 1.18x slower                                                 |
| docutils                   | 4.05 sec                                             | 4.82 sec: 1.19x slower                                                |
| python_startup_no_site     | 16.2 ms                                              | 19.5 ms: 1.20x slower                                                 |
| json_loads                 | 35.9 us                                              | 43.6 us: 1.21x slower                                                 |
| generators                 | 44.7 ms                                              | 54.8 ms: 1.23x slower                                                 |
| deepcopy                   | 486 us                                               | 600 us: 1.23x slower                                                  |
| bench_thread_pool          | 3.42 ms                                              | 4.27 ms: 1.25x slower                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.68 ms: 1.25x slower                                                 |
| json_dumps                 | 14.0 ms                                              | 17.8 ms: 1.27x slower                                                 |
| python_startup             | 22.7 ms                                              | 28.9 ms: 1.28x slower                                                 |
| coroutines                 | 30.6 ms                                              | 39.3 ms: 1.28x slower                                                 |
| pycparser                  | 1.68 sec                                             | 2.18 sec: 1.30x slower                                                |
| tornado_http               | 261 ms                                               | 342 ms: 1.31x slower                                                  |
| mdp                        | 3.77 sec                                             | 5.02 sec: 1.33x slower                                                |
| scimark_fft                | 481 ms                                               | 641 ms: 1.33x slower                                                  |
| comprehensions             | 28.6 us                                              | 38.3 us: 1.34x slower                                                 |
| deepcopy_memo              | 51.0 us                                              | 69.1 us: 1.35x slower                                                 |
| deepcopy_reduce            | 4.18 us                                              | 5.73 us: 1.37x slower                                                 |
| nqueens                    | 116 ms                                               | 162 ms: 1.40x slower                                                  |
| html5lib                   | 100 ms                                               | 141 ms: 1.41x slower                                                  |
| 2to3                       | 456 ms                                               | 647 ms: 1.42x slower                                                  |
| meteor_contest             | 146 ms                                               | 208 ms: 1.42x slower                                                  |
| crypto_pyaes               | 110 ms                                               | 159 ms: 1.45x slower                                                  |
| coverage                   | 96.9 ms                                              | 141 ms: 1.45x slower                                                  |
| bpe_tokeniser              | 6.76 sec                                             | 9.90 sec: 1.47x slower                                                |
| fannkuch                   | 525 ms                                               | 772 ms: 1.47x slower                                                  |
| tomli_loads                | 2.86 sec                                             | 4.22 sec: 1.48x slower                                                |
| telco                      | 9.53 ms                                              | 14.1 ms: 1.48x slower                                                 |
| sympy_integrate            | 29.0 ms                                              | 42.8 ms: 1.48x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 126 ms: 1.53x slower                                                  |
| thrift                     | 1.10 ms                                              | 1.70 ms: 1.54x slower                                                 |
| float                      | 124 ms                                               | 193 ms: 1.55x slower                                                  |
| regex_compile              | 186 ms                                               | 293 ms: 1.57x slower                                                  |
| pyflate                    | 664 ms                                               | 1.07 sec: 1.61x slower                                                |
| typing_runtime_protocols   | 224 us                                               | 362 us: 1.61x slower                                                  |
| logging_simple             | 9.68 us                                              | 15.9 us: 1.64x slower                                                 |
| sqlglot_optimize           | 80.2 ms                                              | 133 ms: 1.66x slower                                                  |
| sqlglot_normalize          | 144 ms                                               | 246 ms: 1.72x slower                                                  |
| genshi_xml                 | 69.1 ms                                              | 120 ms: 1.73x slower                                                  |
| sympy_str                  | 379 ms                                               | 663 ms: 1.75x slower                                                  |
| pprint_pformat             | 1.99 sec                                             | 3.48 sec: 1.75x slower                                                |
| scimark_monte_carlo        | 96.8 ms                                              | 171 ms: 1.76x slower                                                  |
| chaos                      | 92.1 ms                                              | 163 ms: 1.77x slower                                                  |
| richards                   | 62.8 ms                                              | 111 ms: 1.77x slower                                                  |
| django_template            | 45.4 ms                                              | 80.6 ms: 1.78x slower                                                 |
| spectral_norm              | 136 ms                                               | 242 ms: 1.78x slower                                                  |
| pprint_safe_repr           | 972 ms                                               | 1.73 sec: 1.78x slower                                                |
| genshi_text                | 30.3 ms                                              | 54.4 ms: 1.79x slower                                                 |
| richards_super             | 69.7 ms                                              | 125 ms: 1.80x slower                                                  |
| unpickle_pure_python       | 304 us                                               | 558 us: 1.84x slower                                                  |
| logging_format             | 9.56 us                                              | 17.6 us: 1.85x slower                                                 |
| mako                       | 16.1 ms                                              | 29.9 ms: 1.85x slower                                                 |
| logging_silent             | 139 ns                                               | 259 ns: 1.86x slower                                                  |
| pickle_pure_python         | 436 us                                               | 830 us: 1.90x slower                                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.53 ms: 1.95x slower                                                 |
| raytrace                   | 405 ms                                               | 806 ms: 1.99x slower                                                  |
| scimark_lu                 | 155 ms                                               | 313 ms: 2.02x slower                                                  |
| sqlglot_parse              | 1.85 ms                                              | 3.76 ms: 2.03x slower                                                 |
| scimark_sor                | 170 ms                                               | 351 ms: 2.06x slower                                                  |
| hexiom                     | 8.19 ms                                              | 17.4 ms: 2.13x slower                                                 |
| sympy_expand               | 591 ms                                               | 1.27 sec: 2.14x slower                                                |
| sympy_sum                  | 218 ms                                               | 493 ms: 2.26x slower                                                  |
| go                         | 173 ms                                               | 406 ms: 2.35x slower                                                  |
| nbody                      | 117 ms                                               | 280 ms: 2.40x slower                                                  |
| deltablue                  | 4.45 ms                                              | 11.7 ms: 2.62x slower                                                 |
| unpack_sequence            | 70.8 ns                                              | 201 ns: 2.84x slower                                                  |
| Geometric mean             | (ref)                                                | 1.34x slower                                                          |

Benchmark hidden because not significant (5): create_gc_cycles, asyncio_websockets, unpickle, asyncio_tcp, pathlib
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.17x