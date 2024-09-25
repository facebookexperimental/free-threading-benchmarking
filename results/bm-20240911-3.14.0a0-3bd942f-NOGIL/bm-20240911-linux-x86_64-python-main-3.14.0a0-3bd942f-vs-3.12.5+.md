# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 626 ms: 1.37x slower                                  |
| docutils       | 4.05 sec                                             | 4.76 sec: 1.18x slower                                |
| html5lib       | 100 ms                                               | 141 ms: 1.41x slower                                  |
| tornado_http   | 261 ms                                               | 352 ms: 1.35x slower                                  |
| Geometric mean | (ref)                                                | 1.32x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.13 sec: 1.65x faster                                |
| async_tree_none_tg         | 726 ms                                               | 495 ms: 1.47x faster                                  |
| async_tree_none            | 820 ms                                               | 575 ms: 1.42x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.31 sec: 1.42x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 653 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 829 ms: 1.35x faster                                  |
| async_tree_memoization     | 975 ms                                               | 748 ms: 1.30x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 980 ms: 1.17x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.09 sec: 1.11x slower                                |
| async_generators           | 615 ms                                               | 712 ms: 1.16x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.27 sec: 1.16x slower                                |
| coroutines                 | 30.6 ms                                              | 45.1 ms: 1.47x slower                                 |
| Geometric mean             | (ref)                                                | 1.16x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 242 ms: 1.06x faster                                  |
| float          | 124 ms                                               | 201 ms: 1.61x slower                                  |
| nbody          | 117 ms                                               | 312 ms: 2.67x slower                                  |
| Geometric mean | (ref)                                                | 1.60x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.56 ms: 1.10x faster                                 |
| regex_dna      | 268 ms                                               | 284 ms: 1.06x slower                                  |
| regex_v8       | 29.9 ms                                              | 36.1 ms: 1.21x slower                                 |
| regex_compile  | 186 ms                                               | 290 ms: 1.56x slower                                  |
| Geometric mean | (ref)                                                | 1.16x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.01 us                                              | 6.36 us: 1.10x faster                                 |
| pickle               | 15.9 us                                              | 14.9 us: 1.06x faster                                 |
| pickle_dict          | 45.5 us                                              | 43.5 us: 1.05x faster                                 |
| unpickle_list        | 6.83 us                                              | 7.59 us: 1.11x slower                                 |
| xml_etree_generate   | 138 ms                                               | 157 ms: 1.14x slower                                  |
| json_loads           | 35.9 us                                              | 42.8 us: 1.19x slower                                 |
| json_dumps           | 14.0 ms                                              | 18.9 ms: 1.35x slower                                 |
| xml_etree_process    | 82.7 ms                                              | 121 ms: 1.47x slower                                  |
| tomli_loads          | 2.86 sec                                             | 4.35 sec: 1.52x slower                                |
| unpickle_pure_python | 304 us                                               | 547 us: 1.80x slower                                  |
| pickle_pure_python   | 436 us                                               | 804 us: 1.84x slower                                  |
| Geometric mean       | (ref)                                                | 1.20x slower                                          |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 21.2 ms: 1.31x slower                                 |
| python_startup         | 22.7 ms                                              | 30.9 ms: 1.36x slower                                 |
| Geometric mean         | (ref)                                                | 1.34x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 116 ms: 1.68x slower                                  |
| django_template | 45.4 ms                                              | 83.8 ms: 1.85x slower                                 |
| genshi_text     | 30.3 ms                                              | 58.2 ms: 1.92x slower                                 |
| mako            | 16.1 ms                                              | 31.2 ms: 1.93x slower                                 |
| Geometric mean  | (ref)                                                | 1.84x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.13 sec: 1.65x faster                                |
| async_tree_none_tg         | 726 ms                                               | 495 ms: 1.47x faster                                  |
| async_tree_none            | 820 ms                                               | 575 ms: 1.42x faster                                  |
| gc_traversal               | 6.42 ms                                              | 4.51 ms: 1.42x faster                                 |
| async_tree_io              | 1.86 sec                                             | 1.31 sec: 1.42x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 653 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 829 ms: 1.35x faster                                  |
| async_tree_memoization     | 975 ms                                               | 748 ms: 1.30x faster                                  |
| bench_mp_pool              | 21.2 ms                                              | 17.5 ms: 1.21x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 980 ms: 1.17x faster                                  |
| regex_effbot               | 5.02 ms                                              | 4.56 ms: 1.10x faster                                 |
| pickle_list                | 7.01 us                                              | 6.36 us: 1.10x faster                                 |
| create_gc_cycles           | 2.00 ms                                              | 1.83 ms: 1.09x faster                                 |
| pickle                     | 15.9 us                                              | 14.9 us: 1.06x faster                                 |
| pidigits                   | 256 ms                                               | 242 ms: 1.06x faster                                  |
| pickle_dict                | 45.5 us                                              | 43.5 us: 1.05x faster                                 |
| regex_dna                  | 268 ms                                               | 284 ms: 1.06x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.09 sec: 1.11x slower                                |
| sqlite_synth               | 3.77 us                                              | 4.19 us: 1.11x slower                                 |
| unpickle_list              | 6.83 us                                              | 7.59 us: 1.11x slower                                 |
| json                       | 7.14 ms                                              | 7.97 ms: 1.12x slower                                 |
| xml_etree_generate         | 138 ms                                               | 157 ms: 1.14x slower                                  |
| async_generators           | 615 ms                                               | 712 ms: 1.16x slower                                  |
| pathlib                    | 31.6 ms                                              | 36.6 ms: 1.16x slower                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.27 sec: 1.16x slower                                |
| docutils                   | 4.05 sec                                             | 4.76 sec: 1.18x slower                                |
| deepcopy                   | 486 us                                               | 579 us: 1.19x slower                                  |
| json_loads                 | 35.9 us                                              | 42.8 us: 1.19x slower                                 |
| regex_v8                   | 29.9 ms                                              | 36.1 ms: 1.21x slower                                 |
| scimark_fft                | 481 ms                                               | 587 ms: 1.22x slower                                  |
| bench_thread_pool          | 3.42 ms                                              | 4.19 ms: 1.23x slower                                 |
| generators                 | 44.7 ms                                              | 54.8 ms: 1.23x slower                                 |
| pylint                     | 480 ms                                               | 593 ms: 1.24x slower                                  |
| dulwich_log                | 104 ms                                               | 130 ms: 1.25x slower                                  |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.77 ms: 1.26x slower                                 |
| meteor_contest             | 146 ms                                               | 186 ms: 1.27x slower                                  |
| python_startup_no_site     | 16.2 ms                                              | 21.2 ms: 1.31x slower                                 |
| comprehensions             | 28.6 us                                              | 38.4 us: 1.34x slower                                 |
| tornado_http               | 261 ms                                               | 352 ms: 1.35x slower                                  |
| json_dumps                 | 14.0 ms                                              | 18.9 ms: 1.35x slower                                 |
| mdp                        | 3.77 sec                                             | 5.11 sec: 1.36x slower                                |
| pycparser                  | 1.68 sec                                             | 2.28 sec: 1.36x slower                                |
| python_startup             | 22.7 ms                                              | 30.9 ms: 1.36x slower                                 |
| 2to3                       | 456 ms                                               | 626 ms: 1.37x slower                                  |
| crypto_pyaes               | 110 ms                                               | 151 ms: 1.38x slower                                  |
| nqueens                    | 116 ms                                               | 160 ms: 1.38x slower                                  |
| html5lib                   | 100 ms                                               | 141 ms: 1.41x slower                                  |
| deepcopy_reduce            | 4.18 us                                              | 5.88 us: 1.41x slower                                 |
| deepcopy_memo              | 51.0 us                                              | 73.7 us: 1.44x slower                                 |
| fannkuch                   | 525 ms                                               | 767 ms: 1.46x slower                                  |
| xml_etree_process          | 82.7 ms                                              | 121 ms: 1.47x slower                                  |
| telco                      | 9.53 ms                                              | 14.0 ms: 1.47x slower                                 |
| coroutines                 | 30.6 ms                                              | 45.1 ms: 1.47x slower                                 |
| bpe_tokeniser              | 6.76 sec                                             | 10.0 sec: 1.49x slower                                |
| thrift                     | 1.10 ms                                              | 1.65 ms: 1.50x slower                                 |
| sympy_integrate            | 29.0 ms                                              | 43.8 ms: 1.51x slower                                 |
| tomli_loads                | 2.86 sec                                             | 4.35 sec: 1.52x slower                                |
| coverage                   | 96.9 ms                                              | 147 ms: 1.52x slower                                  |
| logging_simple             | 9.68 us                                              | 15.0 us: 1.55x slower                                 |
| sqlglot_optimize           | 80.2 ms                                              | 125 ms: 1.55x slower                                  |
| regex_compile              | 186 ms                                               | 290 ms: 1.56x slower                                  |
| float                      | 124 ms                                               | 201 ms: 1.61x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 157 ms: 1.62x slower                                  |
| pyflate                    | 664 ms                                               | 1.08 sec: 1.62x slower                                |
| typing_runtime_protocols   | 224 us                                               | 364 us: 1.62x slower                                  |
| richards                   | 62.8 ms                                              | 105 ms: 1.67x slower                                  |
| logging_format             | 9.56 us                                              | 16.0 us: 1.67x slower                                 |
| genshi_xml                 | 69.1 ms                                              | 116 ms: 1.68x slower                                  |
| sqlglot_normalize          | 144 ms                                               | 245 ms: 1.71x slower                                  |
| pprint_safe_repr           | 972 ms                                               | 1.69 sec: 1.74x slower                                |
| pprint_pformat             | 1.99 sec                                             | 3.52 sec: 1.77x slower                                |
| sympy_str                  | 379 ms                                               | 672 ms: 1.77x slower                                  |
| unpickle_pure_python       | 304 us                                               | 547 us: 1.80x slower                                  |
| chaos                      | 92.1 ms                                              | 168 ms: 1.82x slower                                  |
| pickle_pure_python         | 436 us                                               | 804 us: 1.84x slower                                  |
| django_template            | 45.4 ms                                              | 83.8 ms: 1.85x slower                                 |
| spectral_norm              | 136 ms                                               | 254 ms: 1.86x slower                                  |
| richards_super             | 69.7 ms                                              | 130 ms: 1.87x slower                                  |
| sqlglot_parse              | 1.85 ms                                              | 3.50 ms: 1.89x slower                                 |
| genshi_text                | 30.3 ms                                              | 58.2 ms: 1.92x slower                                 |
| mako                       | 16.1 ms                                              | 31.2 ms: 1.93x slower                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.53 ms: 1.95x slower                                 |
| logging_silent             | 139 ns                                               | 272 ns: 1.95x slower                                  |
| hexiom                     | 8.19 ms                                              | 16.0 ms: 1.96x slower                                 |
| raytrace                   | 405 ms                                               | 791 ms: 1.96x slower                                  |
| scimark_sor                | 170 ms                                               | 337 ms: 1.98x slower                                  |
| scimark_lu                 | 155 ms                                               | 309 ms: 1.99x slower                                  |
| sympy_sum                  | 218 ms                                               | 464 ms: 2.13x slower                                  |
| go                         | 173 ms                                               | 369 ms: 2.13x slower                                  |
| sympy_expand               | 591 ms                                               | 1.36 sec: 2.29x slower                                |
| deltablue                  | 4.45 ms                                              | 10.9 ms: 2.45x slower                                 |
| unpack_sequence            | 70.8 ns                                              | 187 ns: 2.65x slower                                  |
| nbody                      | 117 ms                                               | 312 ms: 2.67x slower                                  |
| Geometric mean             | (ref)                                                | 1.35x slower                                          |

Benchmark hidden because not significant (4): xml_etree_parse, asyncio_websockets, xml_etree_iterparse, unpickle
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.15x