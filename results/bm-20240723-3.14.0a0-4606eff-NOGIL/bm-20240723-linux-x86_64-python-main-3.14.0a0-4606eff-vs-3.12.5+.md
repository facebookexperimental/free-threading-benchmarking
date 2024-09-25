# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 664 ms: 1.45x slower                                  |
| docutils       | 4.05 sec                                             | 4.86 sec: 1.20x slower                                |
| html5lib       | 100 ms                                               | 157 ms: 1.57x slower                                  |
| tornado_http   | 261 ms                                               | 320 ms: 1.22x slower                                  |
| Geometric mean | (ref)                                                | 1.35x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.22 sec: 1.52x faster                                |
| async_tree_none_tg         | 726 ms                                               | 493 ms: 1.47x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 654 ms: 1.40x faster                                  |
| async_tree_none            | 820 ms                                               | 593 ms: 1.38x faster                                  |
| async_tree_memoization     | 975 ms                                               | 733 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 859 ms: 1.30x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 945 ms: 1.21x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.14x slower                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.27 sec: 1.16x slower                                |
| async_generators           | 615 ms                                               | 724 ms: 1.18x slower                                  |
| coroutines                 | 30.6 ms                                              | 45.6 ms: 1.49x slower                                 |
| Geometric mean             | (ref)                                                | 1.15x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 243 ms: 1.05x faster                                  |
| float          | 124 ms                                               | 200 ms: 1.61x slower                                  |
| nbody          | 117 ms                                               | 283 ms: 2.42x slower                                  |
| Geometric mean | (ref)                                                | 1.55x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.80 ms: 1.05x faster                                 |
| regex_dna      | 268 ms                                               | 301 ms: 1.12x slower                                  |
| regex_v8       | 29.9 ms                                              | 33.7 ms: 1.13x slower                                 |
| regex_compile  | 186 ms                                               | 292 ms: 1.57x slower                                  |
| Geometric mean | (ref)                                                | 1.17x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 213 ms: 1.15x faster                                  |
| pickle               | 15.9 us                                              | 14.3 us: 1.11x faster                                 |
| pickle_list          | 7.01 us                                              | 6.45 us: 1.09x faster                                 |
| pickle_dict          | 45.5 us                                              | 42.9 us: 1.06x faster                                 |
| unpickle_list        | 6.83 us                                              | 7.21 us: 1.06x slower                                 |
| xml_etree_generate   | 138 ms                                               | 158 ms: 1.15x slower                                  |
| json_loads           | 35.9 us                                              | 45.2 us: 1.26x slower                                 |
| json_dumps           | 14.0 ms                                              | 18.9 ms: 1.35x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.14 sec: 1.45x slower                                |
| xml_etree_process    | 82.7 ms                                              | 124 ms: 1.50x slower                                  |
| pickle_pure_python   | 436 us                                               | 760 us: 1.74x slower                                  |
| unpickle_pure_python | 304 us                                               | 540 us: 1.78x slower                                  |
| Geometric mean       | (ref)                                                | 1.17x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 20.9 ms: 1.29x slower                                 |
| python_startup         | 22.7 ms                                              | 29.5 ms: 1.30x slower                                 |
| Geometric mean         | (ref)                                                | 1.29x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 122 ms: 1.77x slower                                  |
| genshi_text     | 30.3 ms                                              | 55.7 ms: 1.84x slower                                 |
| django_template | 45.4 ms                                              | 84.5 ms: 1.86x slower                                 |
| mako            | 16.1 ms                                              | 31.9 ms: 1.97x slower                                 |
| Geometric mean  | (ref)                                                | 1.86x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                |
| bench_mp_pool              | 21.2 ms                                              | 13.3 ms: 1.59x faster                                 |
| async_tree_io              | 1.86 sec                                             | 1.22 sec: 1.52x faster                                |
| async_tree_none_tg         | 726 ms                                               | 493 ms: 1.47x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 654 ms: 1.40x faster                                  |
| gc_traversal               | 6.42 ms                                              | 4.60 ms: 1.39x faster                                 |
| async_tree_none            | 820 ms                                               | 593 ms: 1.38x faster                                  |
| async_tree_memoization     | 975 ms                                               | 733 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 859 ms: 1.30x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 945 ms: 1.21x faster                                  |
| xml_etree_parse            | 244 ms                                               | 213 ms: 1.15x faster                                  |
| pickle                     | 15.9 us                                              | 14.3 us: 1.11x faster                                 |
| create_gc_cycles           | 2.00 ms                                              | 1.82 ms: 1.09x faster                                 |
| pickle_list                | 7.01 us                                              | 6.45 us: 1.09x faster                                 |
| pickle_dict                | 45.5 us                                              | 42.9 us: 1.06x faster                                 |
| pidigits                   | 256 ms                                               | 243 ms: 1.05x faster                                  |
| regex_effbot               | 5.02 ms                                              | 4.80 ms: 1.05x faster                                 |
| unpickle_list              | 6.83 us                                              | 7.21 us: 1.06x slower                                 |
| regex_dna                  | 268 ms                                               | 301 ms: 1.12x slower                                  |
| sqlite_synth               | 3.77 us                                              | 4.23 us: 1.12x slower                                 |
| regex_v8                   | 29.9 ms                                              | 33.7 ms: 1.13x slower                                 |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.14x slower                                |
| xml_etree_generate         | 138 ms                                               | 158 ms: 1.15x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.27 sec: 1.16x slower                                |
| bench_thread_pool          | 3.42 ms                                              | 4.01 ms: 1.17x slower                                 |
| async_generators           | 615 ms                                               | 724 ms: 1.18x slower                                  |
| docutils                   | 4.05 sec                                             | 4.86 sec: 1.20x slower                                |
| json                       | 7.14 ms                                              | 8.61 ms: 1.20x slower                                 |
| pylint                     | 480 ms                                               | 582 ms: 1.21x slower                                  |
| deepcopy                   | 486 us                                               | 594 us: 1.22x slower                                  |
| tornado_http               | 261 ms                                               | 320 ms: 1.22x slower                                  |
| generators                 | 44.7 ms                                              | 54.9 ms: 1.23x slower                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.70 ms: 1.25x slower                                 |
| json_loads                 | 35.9 us                                              | 45.2 us: 1.26x slower                                 |
| scimark_fft                | 481 ms                                               | 617 ms: 1.28x slower                                  |
| python_startup_no_site     | 16.2 ms                                              | 20.9 ms: 1.29x slower                                 |
| pycparser                  | 1.68 sec                                             | 2.16 sec: 1.29x slower                                |
| python_startup             | 22.7 ms                                              | 29.5 ms: 1.30x slower                                 |
| nqueens                    | 116 ms                                               | 152 ms: 1.32x slower                                  |
| comprehensions             | 28.6 us                                              | 38.3 us: 1.34x slower                                 |
| dulwich_log                | 104 ms                                               | 140 ms: 1.34x slower                                  |
| json_dumps                 | 14.0 ms                                              | 18.9 ms: 1.35x slower                                 |
| mdp                        | 3.77 sec                                             | 5.10 sec: 1.35x slower                                |
| meteor_contest             | 146 ms                                               | 199 ms: 1.36x slower                                  |
| deepcopy_memo              | 51.0 us                                              | 69.7 us: 1.36x slower                                 |
| deepcopy_reduce            | 4.18 us                                              | 5.85 us: 1.40x slower                                 |
| telco                      | 9.53 ms                                              | 13.4 ms: 1.40x slower                                 |
| crypto_pyaes               | 110 ms                                               | 157 ms: 1.44x slower                                  |
| tomli_loads                | 2.86 sec                                             | 4.14 sec: 1.45x slower                                |
| 2to3                       | 456 ms                                               | 664 ms: 1.45x slower                                  |
| coroutines                 | 30.6 ms                                              | 45.6 ms: 1.49x slower                                 |
| fannkuch                   | 525 ms                                               | 783 ms: 1.49x slower                                  |
| bpe_tokeniser              | 6.76 sec                                             | 10.1 sec: 1.50x slower                                |
| xml_etree_process          | 82.7 ms                                              | 124 ms: 1.50x slower                                  |
| sympy_integrate            | 29.0 ms                                              | 43.9 ms: 1.52x slower                                 |
| typing_runtime_protocols   | 224 us                                               | 342 us: 1.53x slower                                  |
| sqlglot_optimize           | 80.2 ms                                              | 124 ms: 1.55x slower                                  |
| coverage                   | 96.9 ms                                              | 151 ms: 1.56x slower                                  |
| regex_compile              | 186 ms                                               | 292 ms: 1.57x slower                                  |
| html5lib                   | 100 ms                                               | 157 ms: 1.57x slower                                  |
| logging_simple             | 9.68 us                                              | 15.2 us: 1.57x slower                                 |
| thrift                     | 1.10 ms                                              | 1.75 ms: 1.59x slower                                 |
| sqlglot_normalize          | 144 ms                                               | 230 ms: 1.60x slower                                  |
| float                      | 124 ms                                               | 200 ms: 1.61x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 163 ms: 1.68x slower                                  |
| pyflate                    | 664 ms                                               | 1.13 sec: 1.71x slower                                |
| logging_format             | 9.56 us                                              | 16.6 us: 1.74x slower                                 |
| pickle_pure_python         | 436 us                                               | 760 us: 1.74x slower                                  |
| pprint_safe_repr           | 972 ms                                               | 1.71 sec: 1.76x slower                                |
| logging_silent             | 139 ns                                               | 246 ns: 1.76x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 122 ms: 1.77x slower                                  |
| unpickle_pure_python       | 304 us                                               | 540 us: 1.78x slower                                  |
| richards                   | 62.8 ms                                              | 112 ms: 1.78x slower                                  |
| pprint_pformat             | 1.99 sec                                             | 3.55 sec: 1.79x slower                                |
| sympy_str                  | 379 ms                                               | 685 ms: 1.81x slower                                  |
| spectral_norm              | 136 ms                                               | 247 ms: 1.81x slower                                  |
| genshi_text                | 30.3 ms                                              | 55.7 ms: 1.84x slower                                 |
| django_template            | 45.4 ms                                              | 84.5 ms: 1.86x slower                                 |
| chaos                      | 92.1 ms                                              | 175 ms: 1.90x slower                                  |
| richards_super             | 69.7 ms                                              | 133 ms: 1.91x slower                                  |
| mako                       | 16.1 ms                                              | 31.9 ms: 1.97x slower                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.58 ms: 1.97x slower                                 |
| raytrace                   | 405 ms                                               | 807 ms: 2.00x slower                                  |
| scimark_sor                | 170 ms                                               | 341 ms: 2.00x slower                                  |
| scimark_lu                 | 155 ms                                               | 314 ms: 2.02x slower                                  |
| hexiom                     | 8.19 ms                                              | 16.7 ms: 2.05x slower                                 |
| sympy_expand               | 591 ms                                               | 1.27 sec: 2.15x slower                                |
| sqlglot_parse              | 1.85 ms                                              | 3.99 ms: 2.16x slower                                 |
| sympy_sum                  | 218 ms                                               | 476 ms: 2.18x slower                                  |
| go                         | 173 ms                                               | 411 ms: 2.37x slower                                  |
| nbody                      | 117 ms                                               | 283 ms: 2.42x slower                                  |
| deltablue                  | 4.45 ms                                              | 11.4 ms: 2.56x slower                                 |
| unpack_sequence            | 70.8 ns                                              | 200 ns: 2.83x slower                                  |
| Geometric mean             | (ref)                                                | 1.35x slower                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle, asyncio_websockets, pathlib
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.16x