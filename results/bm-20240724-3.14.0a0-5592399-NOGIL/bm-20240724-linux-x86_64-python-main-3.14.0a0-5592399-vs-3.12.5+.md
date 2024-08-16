# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 662 ms: 1.45x slower                                  |
| docutils       | 4.05 sec                                             | 4.97 sec: 1.23x slower                                |
| html5lib       | 100 ms                                               | 137 ms: 1.37x slower                                  |
| tornado_http   | 261 ms                                               | 339 ms: 1.30x slower                                  |
| Geometric mean | (ref)                                                | 1.33x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.27 sec: 1.46x faster                                |
| async_tree_none_tg         | 726 ms                                               | 514 ms: 1.41x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 652 ms: 1.40x faster                                  |
| async_tree_none            | 820 ms                                               | 586 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 850 ms: 1.32x faster                                  |
| async_tree_memoization     | 975 ms                                               | 759 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 959 ms: 1.19x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.08 sec: 1.09x slower                                |
| async_generators           | 615 ms                                               | 721 ms: 1.17x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.42 sec: 1.21x slower                                |
| coroutines                 | 30.6 ms                                              | 41.7 ms: 1.36x slower                                 |
| Geometric mean             | (ref)                                                | 1.15x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 241 ms: 1.07x faster                                  |
| float          | 124 ms                                               | 211 ms: 1.69x slower                                  |
| nbody          | 117 ms                                               | 278 ms: 2.38x slower                                  |
| Geometric mean | (ref)                                                | 1.56x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.76 ms: 1.05x faster                                 |
| regex_dna      | 268 ms                                               | 287 ms: 1.07x slower                                  |
| regex_v8       | 29.9 ms                                              | 37.6 ms: 1.26x slower                                 |
| regex_compile  | 186 ms                                               | 307 ms: 1.65x slower                                  |
| Geometric mean | (ref)                                                | 1.20x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 208 ms: 1.17x faster                                  |
| pickle               | 15.9 us                                              | 14.4 us: 1.10x faster                                 |
| pickle_list          | 7.01 us                                              | 6.68 us: 1.05x faster                                 |
| unpickle_list        | 6.83 us                                              | 7.97 us: 1.17x slower                                 |
| xml_etree_generate   | 138 ms                                               | 164 ms: 1.19x slower                                  |
| json_loads           | 35.9 us                                              | 45.6 us: 1.27x slower                                 |
| json_dumps           | 14.0 ms                                              | 19.0 ms: 1.35x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.32 sec: 1.51x slower                                |
| xml_etree_process    | 82.7 ms                                              | 127 ms: 1.53x slower                                  |
| unpickle_pure_python | 304 us                                               | 547 us: 1.80x slower                                  |
| pickle_pure_python   | 436 us                                               | 801 us: 1.84x slower                                  |
| Geometric mean       | (ref)                                                | 1.20x slower                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 19.3 ms: 1.19x slower                                 |
| python_startup         | 22.7 ms                                              | 29.1 ms: 1.28x slower                                 |
| Geometric mean         | (ref)                                                | 1.24x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 30.3 ms                                              | 53.7 ms: 1.77x slower                                 |
| genshi_xml      | 69.1 ms                                              | 125 ms: 1.81x slower                                  |
| django_template | 45.4 ms                                              | 86.4 ms: 1.90x slower                                 |
| mako            | 16.1 ms                                              | 31.1 ms: 1.93x slower                                 |
| Geometric mean  | (ref)                                                | 1.85x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                |
| bench_mp_pool              | 21.2 ms                                              | 14.4 ms: 1.47x faster                                 |
| async_tree_io              | 1.86 sec                                             | 1.27 sec: 1.46x faster                                |
| gc_traversal               | 6.42 ms                                              | 4.51 ms: 1.42x faster                                 |
| async_tree_none_tg         | 726 ms                                               | 514 ms: 1.41x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 652 ms: 1.40x faster                                  |
| async_tree_none            | 820 ms                                               | 586 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 850 ms: 1.32x faster                                  |
| async_tree_memoization     | 975 ms                                               | 759 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 959 ms: 1.19x faster                                  |
| xml_etree_parse            | 244 ms                                               | 208 ms: 1.17x faster                                  |
| pickle                     | 15.9 us                                              | 14.4 us: 1.10x faster                                 |
| pidigits                   | 256 ms                                               | 241 ms: 1.07x faster                                  |
| regex_effbot               | 5.02 ms                                              | 4.76 ms: 1.05x faster                                 |
| pickle_list                | 7.01 us                                              | 6.68 us: 1.05x faster                                 |
| regex_dna                  | 268 ms                                               | 287 ms: 1.07x slower                                  |
| pathlib                    | 31.6 ms                                              | 34.2 ms: 1.08x slower                                 |
| asyncio_tcp                | 988 ms                                               | 1.08 sec: 1.09x slower                                |
| json                       | 7.14 ms                                              | 8.11 ms: 1.14x slower                                 |
| deepcopy                   | 486 us                                               | 556 us: 1.14x slower                                  |
| sqlite_synth               | 3.77 us                                              | 4.39 us: 1.16x slower                                 |
| unpickle_list              | 6.83 us                                              | 7.97 us: 1.17x slower                                 |
| async_generators           | 615 ms                                               | 721 ms: 1.17x slower                                  |
| python_startup_no_site     | 16.2 ms                                              | 19.3 ms: 1.19x slower                                 |
| xml_etree_generate         | 138 ms                                               | 164 ms: 1.19x slower                                  |
| generators                 | 44.7 ms                                              | 53.4 ms: 1.19x slower                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.42 sec: 1.21x slower                                |
| docutils                   | 4.05 sec                                             | 4.97 sec: 1.23x slower                                |
| pylint                     | 480 ms                                               | 592 ms: 1.23x slower                                  |
| bench_thread_pool          | 3.42 ms                                              | 4.26 ms: 1.25x slower                                 |
| regex_v8                   | 29.9 ms                                              | 37.6 ms: 1.26x slower                                 |
| json_loads                 | 35.9 us                                              | 45.6 us: 1.27x slower                                 |
| scimark_fft                | 481 ms                                               | 616 ms: 1.28x slower                                  |
| python_startup             | 22.7 ms                                              | 29.1 ms: 1.28x slower                                 |
| dulwich_log                | 104 ms                                               | 134 ms: 1.29x slower                                  |
| tornado_http               | 261 ms                                               | 339 ms: 1.30x slower                                  |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.09 ms: 1.31x slower                                 |
| mdp                        | 3.77 sec                                             | 4.96 sec: 1.31x slower                                |
| pycparser                  | 1.68 sec                                             | 2.25 sec: 1.34x slower                                |
| json_dumps                 | 14.0 ms                                              | 19.0 ms: 1.35x slower                                 |
| meteor_contest             | 146 ms                                               | 198 ms: 1.35x slower                                  |
| coroutines                 | 30.6 ms                                              | 41.7 ms: 1.36x slower                                 |
| html5lib                   | 100 ms                                               | 137 ms: 1.37x slower                                  |
| deepcopy_memo              | 51.0 us                                              | 70.5 us: 1.38x slower                                 |
| crypto_pyaes               | 110 ms                                               | 152 ms: 1.39x slower                                  |
| comprehensions             | 28.6 us                                              | 39.9 us: 1.39x slower                                 |
| nqueens                    | 116 ms                                               | 161 ms: 1.40x slower                                  |
| 2to3                       | 456 ms                                               | 662 ms: 1.45x slower                                  |
| telco                      | 9.53 ms                                              | 13.8 ms: 1.45x slower                                 |
| fannkuch                   | 525 ms                                               | 792 ms: 1.51x slower                                  |
| tomli_loads                | 2.86 sec                                             | 4.32 sec: 1.51x slower                                |
| bpe_tokeniser              | 6.76 sec                                             | 10.2 sec: 1.51x slower                                |
| coverage                   | 96.9 ms                                              | 148 ms: 1.52x slower                                  |
| sympy_integrate            | 29.0 ms                                              | 44.1 ms: 1.52x slower                                 |
| deepcopy_reduce            | 4.18 us                                              | 6.40 us: 1.53x slower                                 |
| sqlglot_optimize           | 80.2 ms                                              | 123 ms: 1.53x slower                                  |
| xml_etree_process          | 82.7 ms                                              | 127 ms: 1.53x slower                                  |
| typing_runtime_protocols   | 224 us                                               | 354 us: 1.58x slower                                  |
| sqlglot_normalize          | 144 ms                                               | 227 ms: 1.58x slower                                  |
| thrift                     | 1.10 ms                                              | 1.74 ms: 1.58x slower                                 |
| regex_compile              | 186 ms                                               | 307 ms: 1.65x slower                                  |
| pyflate                    | 664 ms                                               | 1.12 sec: 1.68x slower                                |
| float                      | 124 ms                                               | 211 ms: 1.69x slower                                  |
| richards                   | 62.8 ms                                              | 107 ms: 1.70x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 164 ms: 1.70x slower                                  |
| logging_simple             | 9.68 us                                              | 16.5 us: 1.71x slower                                 |
| genshi_text                | 30.3 ms                                              | 53.7 ms: 1.77x slower                                 |
| pprint_pformat             | 1.99 sec                                             | 3.52 sec: 1.77x slower                                |
| sympy_str                  | 379 ms                                               | 679 ms: 1.79x slower                                  |
| unpickle_pure_python       | 304 us                                               | 547 us: 1.80x slower                                  |
| pprint_safe_repr           | 972 ms                                               | 1.75 sec: 1.80x slower                                |
| spectral_norm              | 136 ms                                               | 246 ms: 1.80x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 125 ms: 1.81x slower                                  |
| richards_super             | 69.7 ms                                              | 127 ms: 1.83x slower                                  |
| pickle_pure_python         | 436 us                                               | 801 us: 1.84x slower                                  |
| logging_format             | 9.56 us                                              | 17.9 us: 1.87x slower                                 |
| django_template            | 45.4 ms                                              | 86.4 ms: 1.90x slower                                 |
| chaos                      | 92.1 ms                                              | 176 ms: 1.91x slower                                  |
| logging_silent             | 139 ns                                               | 266 ns: 1.91x slower                                  |
| mako                       | 16.1 ms                                              | 31.1 ms: 1.93x slower                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.52 ms: 1.95x slower                                 |
| hexiom                     | 8.19 ms                                              | 16.1 ms: 1.97x slower                                 |
| raytrace                   | 405 ms                                               | 803 ms: 1.99x slower                                  |
| scimark_lu                 | 155 ms                                               | 315 ms: 2.03x slower                                  |
| scimark_sor                | 170 ms                                               | 353 ms: 2.08x slower                                  |
| sympy_expand               | 591 ms                                               | 1.26 sec: 2.14x slower                                |
| sqlglot_parse              | 1.85 ms                                              | 4.03 ms: 2.17x slower                                 |
| sympy_sum                  | 218 ms                                               | 483 ms: 2.22x slower                                  |
| nbody                      | 117 ms                                               | 278 ms: 2.38x slower                                  |
| go                         | 173 ms                                               | 420 ms: 2.43x slower                                  |
| deltablue                  | 4.45 ms                                              | 11.8 ms: 2.64x slower                                 |
| unpack_sequence            | 70.8 ns                                              | 194 ns: 2.74x slower                                  |
| Geometric mean             | (ref)                                                | 1.36x slower                                          |

Benchmark hidden because not significant (5): create_gc_cycles, xml_etree_iterparse, pickle_dict, unpickle, asyncio_websockets
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.16x