# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4767a6e
- commit date: 2024-08-06
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 666 ms: 1.46x slower                                  |
| docutils       | 4.05 sec                                             | 5.00 sec: 1.23x slower                                |
| html5lib       | 100 ms                                               | 162 ms: 1.61x slower                                  |
| tornado_http   | 261 ms                                               | 337 ms: 1.29x slower                                  |
| Geometric mean | (ref)                                                | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.14 sec: 1.64x faster                                |
| async_tree_none_tg         | 726 ms                                               | 483 ms: 1.50x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.24 sec: 1.50x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 634 ms: 1.44x faster                                  |
| async_tree_none            | 820 ms                                               | 607 ms: 1.35x faster                                  |
| async_tree_memoization     | 975 ms                                               | 744 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 909 ms: 1.23x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 961 ms: 1.19x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.11 sec: 1.13x slower                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.33 sec: 1.18x slower                                |
| async_generators           | 615 ms                                               | 740 ms: 1.20x slower                                  |
| coroutines                 | 30.6 ms                                              | 43.8 ms: 1.43x slower                                 |
| Geometric mean             | (ref)                                                | 1.15x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 267 ms: 1.04x slower                                  |
| float          | 124 ms                                               | 190 ms: 1.53x slower                                  |
| nbody          | 117 ms                                               | 309 ms: 2.65x slower                                  |
| Geometric mean | (ref)                                                | 1.62x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 268 ms                                               | 304 ms: 1.13x slower                                  |
| regex_v8       | 29.9 ms                                              | 36.9 ms: 1.23x slower                                 |
| regex_compile  | 186 ms                                               | 288 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                | 1.21x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 15.9 us                                              | 14.1 us: 1.12x faster                                 |
| xml_etree_parse      | 244 ms                                               | 222 ms: 1.10x faster                                  |
| pickle_list          | 7.01 us                                              | 6.56 us: 1.07x faster                                 |
| pickle_dict          | 45.5 us                                              | 42.8 us: 1.06x faster                                 |
| unpickle_list        | 6.83 us                                              | 7.55 us: 1.11x slower                                 |
| unpickle             | 21.6 us                                              | 24.7 us: 1.14x slower                                 |
| xml_etree_generate   | 138 ms                                               | 162 ms: 1.18x slower                                  |
| json_loads           | 35.9 us                                              | 45.4 us: 1.27x slower                                 |
| json_dumps           | 14.0 ms                                              | 18.6 ms: 1.33x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.21 sec: 1.47x slower                                |
| xml_etree_process    | 82.7 ms                                              | 132 ms: 1.59x slower                                  |
| pickle_pure_python   | 436 us                                               | 764 us: 1.75x slower                                  |
| unpickle_pure_python | 304 us                                               | 537 us: 1.77x slower                                  |
| Geometric mean       | (ref)                                                | 1.20x slower                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 19.2 ms: 1.18x slower                                 |
| python_startup         | 22.7 ms                                              | 29.3 ms: 1.29x slower                                 |
| Geometric mean         | (ref)                                                | 1.24x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 123 ms: 1.78x slower                                  |
| django_template | 45.4 ms                                              | 81.9 ms: 1.80x slower                                 |
| genshi_text     | 30.3 ms                                              | 56.5 ms: 1.86x slower                                 |
| mako            | 16.1 ms                                              | 30.3 ms: 1.88x slower                                 |
| Geometric mean  | (ref)                                                | 1.83x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.14 sec: 1.64x faster                                |
| async_tree_none_tg         | 726 ms                                               | 483 ms: 1.50x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.24 sec: 1.50x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 634 ms: 1.44x faster                                  |
| async_tree_none            | 820 ms                                               | 607 ms: 1.35x faster                                  |
| bench_mp_pool              | 21.2 ms                                              | 16.0 ms: 1.33x faster                                 |
| async_tree_memoization     | 975 ms                                               | 744 ms: 1.31x faster                                  |
| gc_traversal               | 6.42 ms                                              | 5.03 ms: 1.28x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 909 ms: 1.23x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 961 ms: 1.19x faster                                  |
| pickle                     | 15.9 us                                              | 14.1 us: 1.12x faster                                 |
| xml_etree_parse            | 244 ms                                               | 222 ms: 1.10x faster                                  |
| pickle_list                | 7.01 us                                              | 6.56 us: 1.07x faster                                 |
| pickle_dict                | 45.5 us                                              | 42.8 us: 1.06x faster                                 |
| pidigits                   | 256 ms                                               | 267 ms: 1.04x slower                                  |
| pathlib                    | 31.6 ms                                              | 33.6 ms: 1.06x slower                                 |
| unpickle_list              | 6.83 us                                              | 7.55 us: 1.11x slower                                 |
| sqlite_synth               | 3.77 us                                              | 4.22 us: 1.12x slower                                 |
| asyncio_tcp                | 988 ms                                               | 1.11 sec: 1.13x slower                                |
| regex_dna                  | 268 ms                                               | 304 ms: 1.13x slower                                  |
| unpickle                   | 21.6 us                                              | 24.7 us: 1.14x slower                                 |
| xml_etree_generate         | 138 ms                                               | 162 ms: 1.18x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.33 sec: 1.18x slower                                |
| python_startup_no_site     | 16.2 ms                                              | 19.2 ms: 1.18x slower                                 |
| generators                 | 44.7 ms                                              | 53.8 ms: 1.20x slower                                 |
| async_generators           | 615 ms                                               | 740 ms: 1.20x slower                                  |
| pylint                     | 480 ms                                               | 591 ms: 1.23x slower                                  |
| regex_v8                   | 29.9 ms                                              | 36.9 ms: 1.23x slower                                 |
| docutils                   | 4.05 sec                                             | 5.00 sec: 1.23x slower                                |
| deepcopy                   | 486 us                                               | 602 us: 1.24x slower                                  |
| json                       | 7.14 ms                                              | 8.93 ms: 1.25x slower                                 |
| json_loads                 | 35.9 us                                              | 45.4 us: 1.27x slower                                 |
| tornado_http               | 261 ms                                               | 337 ms: 1.29x slower                                  |
| python_startup             | 22.7 ms                                              | 29.3 ms: 1.29x slower                                 |
| bench_thread_pool          | 3.42 ms                                              | 4.44 ms: 1.30x slower                                 |
| mdp                        | 3.77 sec                                             | 5.00 sec: 1.33x slower                                |
| json_dumps                 | 14.0 ms                                              | 18.6 ms: 1.33x slower                                 |
| pycparser                  | 1.68 sec                                             | 2.23 sec: 1.33x slower                                |
| scimark_fft                | 481 ms                                               | 651 ms: 1.35x slower                                  |
| nqueens                    | 116 ms                                               | 161 ms: 1.39x slower                                  |
| crypto_pyaes               | 110 ms                                               | 154 ms: 1.40x slower                                  |
| deepcopy_memo              | 51.0 us                                              | 72.1 us: 1.41x slower                                 |
| deepcopy_reduce            | 4.18 us                                              | 5.96 us: 1.43x slower                                 |
| coroutines                 | 30.6 ms                                              | 43.8 ms: 1.43x slower                                 |
| bpe_tokeniser              | 6.76 sec                                             | 9.70 sec: 1.44x slower                                |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.98 ms: 1.44x slower                                 |
| meteor_contest             | 146 ms                                               | 212 ms: 1.45x slower                                  |
| 2to3                       | 456 ms                                               | 666 ms: 1.46x slower                                  |
| comprehensions             | 28.6 us                                              | 41.9 us: 1.46x slower                                 |
| tomli_loads                | 2.86 sec                                             | 4.21 sec: 1.47x slower                                |
| sqlglot_optimize           | 80.2 ms                                              | 122 ms: 1.52x slower                                  |
| sympy_integrate            | 29.0 ms                                              | 44.2 ms: 1.53x slower                                 |
| float                      | 124 ms                                               | 190 ms: 1.53x slower                                  |
| fannkuch                   | 525 ms                                               | 806 ms: 1.54x slower                                  |
| regex_compile              | 186 ms                                               | 288 ms: 1.54x slower                                  |
| telco                      | 9.53 ms                                              | 14.8 ms: 1.55x slower                                 |
| logging_simple             | 9.68 us                                              | 15.1 us: 1.56x slower                                 |
| xml_etree_process          | 82.7 ms                                              | 132 ms: 1.59x slower                                  |
| html5lib                   | 100 ms                                               | 162 ms: 1.61x slower                                  |
| thrift                     | 1.10 ms                                              | 1.78 ms: 1.61x slower                                 |
| coverage                   | 96.9 ms                                              | 157 ms: 1.63x slower                                  |
| sqlglot_normalize          | 144 ms                                               | 237 ms: 1.65x slower                                  |
| pyflate                    | 664 ms                                               | 1.10 sec: 1.66x slower                                |
| pprint_safe_repr           | 972 ms                                               | 1.65 sec: 1.70x slower                                |
| typing_runtime_protocols   | 224 us                                               | 383 us: 1.71x slower                                  |
| pprint_pformat             | 1.99 sec                                             | 3.44 sec: 1.73x slower                                |
| scimark_monte_carlo        | 96.8 ms                                              | 168 ms: 1.74x slower                                  |
| pickle_pure_python         | 436 us                                               | 764 us: 1.75x slower                                  |
| unpickle_pure_python       | 304 us                                               | 537 us: 1.77x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 123 ms: 1.78x slower                                  |
| django_template            | 45.4 ms                                              | 81.9 ms: 1.80x slower                                 |
| spectral_norm              | 136 ms                                               | 247 ms: 1.81x slower                                  |
| richards_super             | 69.7 ms                                              | 127 ms: 1.82x slower                                  |
| sympy_str                  | 379 ms                                               | 698 ms: 1.84x slower                                  |
| richards                   | 62.8 ms                                              | 116 ms: 1.85x slower                                  |
| genshi_text                | 30.3 ms                                              | 56.5 ms: 1.86x slower                                 |
| mako                       | 16.1 ms                                              | 30.3 ms: 1.88x slower                                 |
| logging_silent             | 139 ns                                               | 267 ns: 1.92x slower                                  |
| chaos                      | 92.1 ms                                              | 179 ms: 1.94x slower                                  |
| logging_format             | 9.56 us                                              | 18.8 us: 1.96x slower                                 |
| hexiom                     | 8.19 ms                                              | 16.2 ms: 1.98x slower                                 |
| raytrace                   | 405 ms                                               | 800 ms: 1.98x slower                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.65 ms: 2.01x slower                                 |
| scimark_sor                | 170 ms                                               | 347 ms: 2.04x slower                                  |
| sqlglot_parse              | 1.85 ms                                              | 3.79 ms: 2.04x slower                                 |
| sympy_sum                  | 218 ms                                               | 470 ms: 2.16x slower                                  |
| scimark_lu                 | 155 ms                                               | 336 ms: 2.17x slower                                  |
| sympy_expand               | 591 ms                                               | 1.30 sec: 2.20x slower                                |
| go                         | 173 ms                                               | 457 ms: 2.64x slower                                  |
| nbody                      | 117 ms                                               | 309 ms: 2.65x slower                                  |
| deltablue                  | 4.45 ms                                              | 11.9 ms: 2.66x slower                                 |
| unpack_sequence            | 70.8 ns                                              | 217 ns: 3.06x slower                                  |
| Geometric mean             | (ref)                                                | 1.38x slower                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, asyncio_websockets, regex_effbot, create_gc_cycles
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.15x