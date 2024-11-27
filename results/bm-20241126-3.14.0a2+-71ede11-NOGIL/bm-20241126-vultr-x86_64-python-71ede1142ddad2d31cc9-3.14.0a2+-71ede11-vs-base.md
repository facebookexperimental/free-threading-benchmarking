# Results vs. base

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.277x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                                                            | 380 ms: 1.47x slower                                                                                                    |
| docutils       | 2.63 sec                                                                                                          | 3.19 sec: 1.21x slower                                                                                                  |
| sphinx         | 1.03 sec                                                                                                          | 1.23 sec: 1.20x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 664 ms                                                                                                            | 633 ms: 1.05x faster                                                                                                    |
| asyncio_websockets         | 523 ms                                                                                                            | 520 ms: 1.01x faster                                                                                                    |
| async_tree_io              | 855 ms                                                                                                            | 905 ms: 1.06x slower                                                                                                    |
| async_tree_none_tg         | 347 ms                                                                                                            | 372 ms: 1.07x slower                                                                                                    |
| async_tree_memoization_tg  | 391 ms                                                                                                            | 469 ms: 1.20x slower                                                                                                    |
| async_tree_memoization     | 409 ms                                                                                                            | 496 ms: 1.21x slower                                                                                                    |
| async_tree_none            | 333 ms                                                                                                            | 406 ms: 1.22x slower                                                                                                    |
| coroutines                 | 22.4 ms                                                                                                           | 28.0 ms: 1.25x slower                                                                                                   |
| async_generators           | 370 ms                                                                                                            | 468 ms: 1.27x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 225 ms                                                                                                            | 184 ms: 1.22x faster                                                                                                    |
| nbody          | 95.1 ms                                                                                                           | 141 ms: 1.48x slower                                                                                                    |
| float          | 80.5 ms                                                                                                           | 144 ms: 1.79x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.79 ms                                                                                                           | 2.84 ms: 1.02x slower                                                                                                   |
| regex_dna      | 180 ms                                                                                                            | 184 ms: 1.02x slower                                                                                                    |
| regex_v8       | 23.6 ms                                                                                                           | 24.6 ms: 1.05x slower                                                                                                   |
| regex_compile  | 135 ms                                                                                                            | 195 ms: 1.45x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 138 ms                                                                                                            | 131 ms: 1.05x faster                                                                                                    |
| xml_etree_iterparse  | 98.9 ms                                                                                                           | 95.0 ms: 1.04x faster                                                                                                   |
| json_loads           | 25.0 us                                                                                                           | 28.2 us: 1.13x slower                                                                                                   |
| xml_etree_generate   | 85.9 ms                                                                                                           | 102 ms: 1.19x slower                                                                                                    |
| json_dumps           | 11.6 ms                                                                                                           | 14.5 ms: 1.25x slower                                                                                                   |
| xml_etree_process    | 60.9 ms                                                                                                           | 82.8 ms: 1.36x slower                                                                                                   |
| tomli_loads          | 2.13 sec                                                                                                          | 2.92 sec: 1.37x slower                                                                                                  |
| unpickle_pure_python | 218 us                                                                                                            | 376 us: 1.73x slower                                                                                                    |
| pickle_pure_python   | 320 us                                                                                                            | 554 us: 1.73x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 17.5 ms: 1.19x slower                                                                                                   |
| python_startup_no_site | 7.44 ms                                                                                                           | 10.3 ms: 1.38x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 50.9 ms                                                                                                           | 68.1 ms: 1.34x slower                                                                                                   |
| genshi_text     | 22.6 ms                                                                                                           | 34.4 ms: 1.53x slower                                                                                                   |
| django_template | 35.5 ms                                                                                                           | 55.7 ms: 1.57x slower                                                                                                   |
| mako            | 11.4 ms                                                                                                           | 19.6 ms: 1.71x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.53x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits                   | 225 ms                                                                                                            | 184 ms: 1.22x faster                                                                                                    |
| gc_traversal               | 3.95 ms                                                                                                           | 3.30 ms: 1.20x faster                                                                                                   |
| create_gc_cycles           | 1.95 ms                                                                                                           | 1.82 ms: 1.08x faster                                                                                                   |
| xml_etree_parse            | 138 ms                                                                                                            | 131 ms: 1.05x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 664 ms                                                                                                            | 633 ms: 1.05x faster                                                                                                    |
| xml_etree_iterparse        | 98.9 ms                                                                                                           | 95.0 ms: 1.04x faster                                                                                                   |
| asyncio_websockets         | 523 ms                                                                                                            | 520 ms: 1.01x faster                                                                                                    |
| regex_effbot               | 2.79 ms                                                                                                           | 2.84 ms: 1.02x slower                                                                                                   |
| regex_dna                  | 180 ms                                                                                                            | 184 ms: 1.02x slower                                                                                                    |
| regex_v8                   | 23.6 ms                                                                                                           | 24.6 ms: 1.05x slower                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.31 us: 1.05x slower                                                                                                   |
| async_tree_io              | 855 ms                                                                                                            | 905 ms: 1.06x slower                                                                                                    |
| async_tree_none_tg         | 347 ms                                                                                                            | 372 ms: 1.07x slower                                                                                                    |
| json                       | 4.60 ms                                                                                                           | 5.15 ms: 1.12x slower                                                                                                   |
| pathlib                    | 18.5 ms                                                                                                           | 20.7 ms: 1.12x slower                                                                                                   |
| json_loads                 | 25.0 us                                                                                                           | 28.2 us: 1.13x slower                                                                                                   |
| mdp                        | 2.49 sec                                                                                                          | 2.89 sec: 1.16x slower                                                                                                  |
| scimark_fft                | 338 ms                                                                                                            | 402 ms: 1.19x slower                                                                                                    |
| xml_etree_generate         | 85.9 ms                                                                                                           | 102 ms: 1.19x slower                                                                                                    |
| python_startup             | 14.7 ms                                                                                                           | 17.5 ms: 1.19x slower                                                                                                   |
| sphinx                     | 1.03 sec                                                                                                          | 1.23 sec: 1.20x slower                                                                                                  |
| async_tree_memoization_tg  | 391 ms                                                                                                            | 469 ms: 1.20x slower                                                                                                    |
| async_tree_memoization     | 409 ms                                                                                                            | 496 ms: 1.21x slower                                                                                                    |
| docutils                   | 2.63 sec                                                                                                          | 3.19 sec: 1.21x slower                                                                                                  |
| spectral_norm              | 110 ms                                                                                                            | 133 ms: 1.21x slower                                                                                                    |
| async_tree_none            | 333 ms                                                                                                            | 406 ms: 1.22x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.70 ms                                                                                                           | 5.76 ms: 1.23x slower                                                                                                   |
| telco                      | 7.30 ms                                                                                                           | 9.00 ms: 1.23x slower                                                                                                   |
| coroutines                 | 22.4 ms                                                                                                           | 28.0 ms: 1.25x slower                                                                                                   |
| json_dumps                 | 11.6 ms                                                                                                           | 14.5 ms: 1.25x slower                                                                                                   |
| bpe_tokeniser              | 4.44 sec                                                                                                          | 5.58 sec: 1.26x slower                                                                                                  |
| async_generators           | 370 ms                                                                                                            | 468 ms: 1.27x slower                                                                                                    |
| bench_mp_pool              | 86.4 ms                                                                                                           | 110 ms: 1.27x slower                                                                                                    |
| shortest_path              | 444 ms                                                                                                            | 565 ms: 1.27x slower                                                                                                    |
| coverage                   | 79.7 ms                                                                                                           | 102 ms: 1.28x slower                                                                                                    |
| connected_components       | 402 ms                                                                                                            | 514 ms: 1.28x slower                                                                                                    |
| dulwich_log                | 76.2 ms                                                                                                           | 99.5 ms: 1.31x slower                                                                                                   |
| many_optionals             | 1.03 ms                                                                                                           | 1.36 ms: 1.32x slower                                                                                                   |
| generators                 | 29.6 ms                                                                                                           | 39.3 ms: 1.33x slower                                                                                                   |
| typing_runtime_protocols   | 158 us                                                                                                            | 211 us: 1.33x slower                                                                                                    |
| genshi_xml                 | 50.9 ms                                                                                                           | 68.1 ms: 1.34x slower                                                                                                   |
| meteor_contest             | 101 ms                                                                                                            | 136 ms: 1.35x slower                                                                                                    |
| xml_etree_process          | 60.9 ms                                                                                                           | 82.8 ms: 1.36x slower                                                                                                   |
| nqueens                    | 78.8 ms                                                                                                           | 108 ms: 1.37x slower                                                                                                    |
| deepcopy                   | 261 us                                                                                                            | 358 us: 1.37x slower                                                                                                    |
| tomli_loads                | 2.13 sec                                                                                                          | 2.92 sec: 1.37x slower                                                                                                  |
| python_startup_no_site     | 7.44 ms                                                                                                           | 10.3 ms: 1.38x slower                                                                                                   |
| sqlglot_optimize           | 53.8 ms                                                                                                           | 75.5 ms: 1.40x slower                                                                                                   |
| sqlglot_normalize          | 107 ms                                                                                                            | 151 ms: 1.41x slower                                                                                                    |
| pycparser                  | 1.13 sec                                                                                                          | 1.60 sec: 1.41x slower                                                                                                  |
| deepcopy_reduce            | 2.66 us                                                                                                           | 3.80 us: 1.43x slower                                                                                                   |
| regex_compile              | 135 ms                                                                                                            | 195 ms: 1.45x slower                                                                                                    |
| fannkuch                   | 374 ms                                                                                                            | 545 ms: 1.46x slower                                                                                                    |
| pprint_safe_repr           | 728 ms                                                                                                            | 1.07 sec: 1.47x slower                                                                                                  |
| pylint                     | 270 ms                                                                                                            | 396 ms: 1.47x slower                                                                                                    |
| 2to3                       | 258 ms                                                                                                            | 380 ms: 1.47x slower                                                                                                    |
| nbody                      | 95.1 ms                                                                                                           | 141 ms: 1.48x slower                                                                                                    |
| deepcopy_memo              | 30.2 us                                                                                                           | 45.4 us: 1.50x slower                                                                                                   |
| subparsers                 | 22.3 ms                                                                                                           | 33.5 ms: 1.50x slower                                                                                                   |
| pprint_pformat             | 1.46 sec                                                                                                          | 2.23 sec: 1.52x slower                                                                                                  |
| genshi_text                | 22.6 ms                                                                                                           | 34.4 ms: 1.53x slower                                                                                                   |
| crypto_pyaes               | 67.7 ms                                                                                                           | 103 ms: 1.53x slower                                                                                                    |
| sympy_integrate            | 19.9 ms                                                                                                           | 31.0 ms: 1.55x slower                                                                                                   |
| django_template            | 35.5 ms                                                                                                           | 55.7 ms: 1.57x slower                                                                                                   |
| thrift                     | 743 us                                                                                                            | 1.21 ms: 1.62x slower                                                                                                   |
| pyflate                    | 453 ms                                                                                                            | 737 ms: 1.63x slower                                                                                                    |
| comprehensions             | 17.4 us                                                                                                           | 29.1 us: 1.67x slower                                                                                                   |
| mako                       | 11.4 ms                                                                                                           | 19.6 ms: 1.71x slower                                                                                                   |
| unpickle_pure_python       | 218 us                                                                                                            | 376 us: 1.73x slower                                                                                                    |
| pickle_pure_python         | 320 us                                                                                                            | 554 us: 1.73x slower                                                                                                    |
| scimark_lu                 | 114 ms                                                                                                            | 199 ms: 1.75x slower                                                                                                    |
| richards                   | 47.4 ms                                                                                                           | 84.6 ms: 1.78x slower                                                                                                   |
| float                      | 80.5 ms                                                                                                           | 144 ms: 1.79x slower                                                                                                    |
| logging_simple             | 6.32 us                                                                                                           | 11.4 us: 1.80x slower                                                                                                   |
| logging_format             | 7.06 us                                                                                                           | 12.7 us: 1.80x slower                                                                                                   |
| logging_silent             | 110 ns                                                                                                            | 199 ns: 1.81x slower                                                                                                    |
| sympy_str                  | 274 ms                                                                                                            | 498 ms: 1.81x slower                                                                                                    |
| scimark_sor                | 134 ms                                                                                                            | 243 ms: 1.82x slower                                                                                                    |
| hexiom                     | 6.10 ms                                                                                                           | 11.4 ms: 1.86x slower                                                                                                   |
| richards_super             | 54.1 ms                                                                                                           | 101 ms: 1.86x slower                                                                                                    |
| scimark_monte_carlo        | 65.6 ms                                                                                                           | 122 ms: 1.87x slower                                                                                                    |
| sqlglot_transpile          | 1.60 ms                                                                                                           | 3.09 ms: 1.93x slower                                                                                                   |
| chaos                      | 58.6 ms                                                                                                           | 116 ms: 1.97x slower                                                                                                    |
| sqlglot_parse              | 1.30 ms                                                                                                           | 2.68 ms: 2.06x slower                                                                                                   |
| sympy_expand               | 464 ms                                                                                                            | 987 ms: 2.13x slower                                                                                                    |
| raytrace                   | 267 ms                                                                                                            | 608 ms: 2.27x slower                                                                                                    |
| go                         | 122 ms                                                                                                            | 285 ms: 2.33x slower                                                                                                    |
| sympy_sum                  | 154 ms                                                                                                            | 360 ms: 2.34x slower                                                                                                    |
| deltablue                  | 3.32 ms                                                                                                           | 8.87 ms: 2.67x slower                                                                                                   |
| bench_thread_pool          | 1.02 ms                                                                                                           | 3.41 ms: 3.33x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.40x slower                                                                                                            |

Benchmark hidden because not significant (3): k_core, async_tree_cpu_io_mixed, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: html5lib

- Geometric mean (including insignificant results): 1.277x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.19x