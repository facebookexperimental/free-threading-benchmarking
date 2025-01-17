# Results vs. base

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.126x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 302 ms: 1.20x slower                                                                                                    |
| docutils       | 2.57 sec                                                                                                          | 2.79 sec: 1.08x slower                                                                                                  |
| sphinx         | 982 ms                                                                                                            | 1.11 sec: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg         | 256 ms                                                                                                            | 239 ms: 1.07x faster                                                                                                    |
| async_tree_io_tg           | 616 ms                                                                                                            | 576 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 511 ms                                                                                                            | 493 ms: 1.04x faster                                                                                                    |
| async_tree_io              | 612 ms                                                                                                            | 601 ms: 1.02x faster                                                                                                    |
| asyncio_websockets         | 522 ms                                                                                                            | 515 ms: 1.01x faster                                                                                                    |
| async_tree_memoization_tg  | 304 ms                                                                                                            | 308 ms: 1.01x slower                                                                                                    |
| async_tree_none            | 274 ms                                                                                                            | 287 ms: 1.05x slower                                                                                                    |
| async_tree_memoization     | 329 ms                                                                                                            | 349 ms: 1.06x slower                                                                                                    |
| coroutines                 | 21.3 ms                                                                                                           | 24.2 ms: 1.14x slower                                                                                                   |
| async_generators           | 321 ms                                                                                                            | 367 ms: 1.14x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 207 ms                                                                                                            | 190 ms: 1.09x faster                                                                                                    |
| float          | 72.2 ms                                                                                                           | 73.4 ms: 1.02x slower                                                                                                   |
| nbody          | 86.5 ms                                                                                                           | 134 ms: 1.54x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.9 ms                                                                                                           | 23.1 ms: 1.03x faster                                                                                                   |
| regex_effbot   | 2.61 ms                                                                                                           | 2.79 ms: 1.07x slower                                                                                                   |
| regex_dna      | 170 ms                                                                                                            | 183 ms: 1.08x slower                                                                                                    |
| regex_compile  | 126 ms                                                                                                            | 150 ms: 1.18x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.0 ms                                                                                                           | 87.7 ms: 1.04x faster                                                                                                   |
| xml_etree_parse      | 129 ms                                                                                                            | 127 ms: 1.01x faster                                                                                                    |
| json_dumps           | 11.6 ms                                                                                                           | 12.7 ms: 1.10x slower                                                                                                   |
| json_loads           | 27.6 us                                                                                                           | 30.7 us: 1.11x slower                                                                                                   |
| unpickle_pure_python | 217 us                                                                                                            | 245 us: 1.13x slower                                                                                                    |
| xml_etree_generate   | 84.4 ms                                                                                                           | 96.1 ms: 1.14x slower                                                                                                   |
| xml_etree_process    | 59.7 ms                                                                                                           | 68.7 ms: 1.15x slower                                                                                                   |
| pickle_pure_python   | 316 us                                                                                                            | 373 us: 1.18x slower                                                                                                    |
| tomli_loads          | 1.86 sec                                                                                                          | 2.30 sec: 1.24x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.2 ms: 1.03x slower                                                                                                   |
| python_startup_no_site | 7.47 ms                                                                                                           | 9.54 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                                                           | 43.4 ms: 1.20x slower                                                                                                   |
| genshi_xml      | 48.2 ms                                                                                                           | 60.2 ms: 1.25x slower                                                                                                   |
| genshi_text     | 21.2 ms                                                                                                           | 27.5 ms: 1.30x slower                                                                                                   |
| mako            | 11.7 ms                                                                                                           | 15.6 ms: 1.33x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.27x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.45 ms                                                                                                           | 3.13 ms: 1.42x faster                                                                                                   |
| create_gc_cycles           | 1.83 ms                                                                                                           | 1.34 ms: 1.37x faster                                                                                                   |
| pidigits                   | 207 ms                                                                                                            | 190 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 256 ms                                                                                                            | 239 ms: 1.07x faster                                                                                                    |
| sqlite_synth               | 2.17 us                                                                                                           | 2.03 us: 1.07x faster                                                                                                   |
| async_tree_io_tg           | 616 ms                                                                                                            | 576 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 511 ms                                                                                                            | 493 ms: 1.04x faster                                                                                                    |
| xml_etree_iterparse        | 91.0 ms                                                                                                           | 87.7 ms: 1.04x faster                                                                                                   |
| regex_v8                   | 23.9 ms                                                                                                           | 23.1 ms: 1.03x faster                                                                                                   |
| async_tree_io              | 612 ms                                                                                                            | 601 ms: 1.02x faster                                                                                                    |
| asyncio_websockets         | 522 ms                                                                                                            | 515 ms: 1.01x faster                                                                                                    |
| xml_etree_parse            | 129 ms                                                                                                            | 127 ms: 1.01x faster                                                                                                    |
| async_tree_memoization_tg  | 304 ms                                                                                                            | 308 ms: 1.01x slower                                                                                                    |
| float                      | 72.2 ms                                                                                                           | 73.4 ms: 1.02x slower                                                                                                   |
| logging_silent             | 107 ns                                                                                                            | 110 ns: 1.03x slower                                                                                                    |
| python_startup             | 14.7 ms                                                                                                           | 15.2 ms: 1.03x slower                                                                                                   |
| pathlib                    | 17.9 ms                                                                                                           | 18.6 ms: 1.04x slower                                                                                                   |
| async_tree_none            | 274 ms                                                                                                            | 287 ms: 1.05x slower                                                                                                    |
| async_tree_memoization     | 329 ms                                                                                                            | 349 ms: 1.06x slower                                                                                                    |
| bench_mp_pool              | 88.6 ms                                                                                                           | 94.2 ms: 1.06x slower                                                                                                   |
| pycparser                  | 1.11 sec                                                                                                          | 1.19 sec: 1.07x slower                                                                                                  |
| regex_effbot               | 2.61 ms                                                                                                           | 2.79 ms: 1.07x slower                                                                                                   |
| json                       | 4.97 ms                                                                                                           | 5.34 ms: 1.07x slower                                                                                                   |
| regex_dna                  | 170 ms                                                                                                            | 183 ms: 1.08x slower                                                                                                    |
| dulwich_log                | 75.6 ms                                                                                                           | 81.9 ms: 1.08x slower                                                                                                   |
| docutils                   | 2.57 sec                                                                                                          | 2.79 sec: 1.08x slower                                                                                                  |
| mdp                        | 2.47 sec                                                                                                          | 2.69 sec: 1.09x slower                                                                                                  |
| json_dumps                 | 11.6 ms                                                                                                           | 12.7 ms: 1.10x slower                                                                                                   |
| json_loads                 | 27.6 us                                                                                                           | 30.7 us: 1.11x slower                                                                                                   |
| generators                 | 28.0 ms                                                                                                           | 31.3 ms: 1.12x slower                                                                                                   |
| bpe_tokeniser              | 4.21 sec                                                                                                          | 4.72 sec: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 217 us                                                                                                            | 245 us: 1.13x slower                                                                                                    |
| k_core                     | 2.04 sec                                                                                                          | 2.31 sec: 1.13x slower                                                                                                  |
| scimark_sor                | 115 ms                                                                                                            | 130 ms: 1.13x slower                                                                                                    |
| sphinx                     | 982 ms                                                                                                            | 1.11 sec: 1.13x slower                                                                                                  |
| pylint                     | 280 ms                                                                                                            | 317 ms: 1.13x slower                                                                                                    |
| subparsers                 | 22.2 ms                                                                                                           | 25.2 ms: 1.14x slower                                                                                                   |
| coroutines                 | 21.3 ms                                                                                                           | 24.2 ms: 1.14x slower                                                                                                   |
| xml_etree_generate         | 84.4 ms                                                                                                           | 96.1 ms: 1.14x slower                                                                                                   |
| many_optionals             | 1.03 ms                                                                                                           | 1.17 ms: 1.14x slower                                                                                                   |
| async_generators           | 321 ms                                                                                                            | 367 ms: 1.14x slower                                                                                                    |
| sqlglot_normalize          | 105 ms                                                                                                            | 121 ms: 1.15x slower                                                                                                    |
| xml_etree_process          | 59.7 ms                                                                                                           | 68.7 ms: 1.15x slower                                                                                                   |
| spectral_norm              | 89.1 ms                                                                                                           | 103 ms: 1.16x slower                                                                                                    |
| logging_simple             | 6.18 us                                                                                                           | 7.15 us: 1.16x slower                                                                                                   |
| pprint_safe_repr           | 700 ms                                                                                                            | 816 ms: 1.17x slower                                                                                                    |
| pprint_pformat             | 1.44 sec                                                                                                          | 1.68 sec: 1.17x slower                                                                                                  |
| sqlglot_optimize           | 52.5 ms                                                                                                           | 61.5 ms: 1.17x slower                                                                                                   |
| logging_format             | 6.96 us                                                                                                           | 8.18 us: 1.18x slower                                                                                                   |
| telco                      | 7.24 ms                                                                                                           | 8.52 ms: 1.18x slower                                                                                                   |
| go                         | 115 ms                                                                                                            | 136 ms: 1.18x slower                                                                                                    |
| pickle_pure_python         | 316 us                                                                                                            | 373 us: 1.18x slower                                                                                                    |
| sympy_expand               | 459 ms                                                                                                            | 543 ms: 1.18x slower                                                                                                    |
| regex_compile              | 126 ms                                                                                                            | 150 ms: 1.18x slower                                                                                                    |
| pyflate                    | 414 ms                                                                                                            | 491 ms: 1.19x slower                                                                                                    |
| deepcopy                   | 259 us                                                                                                            | 310 us: 1.19x slower                                                                                                    |
| 2to3                       | 252 ms                                                                                                            | 302 ms: 1.20x slower                                                                                                    |
| django_template            | 36.1 ms                                                                                                           | 43.4 ms: 1.20x slower                                                                                                   |
| scimark_fft                | 309 ms                                                                                                            | 372 ms: 1.21x slower                                                                                                    |
| scimark_lu                 | 111 ms                                                                                                            | 134 ms: 1.21x slower                                                                                                    |
| sympy_sum                  | 153 ms                                                                                                            | 186 ms: 1.21x slower                                                                                                    |
| thrift                     | 745 us                                                                                                            | 908 us: 1.22x slower                                                                                                    |
| sympy_str                  | 272 ms                                                                                                            | 332 ms: 1.22x slower                                                                                                    |
| sqlglot_transpile          | 1.55 ms                                                                                                           | 1.89 ms: 1.22x slower                                                                                                   |
| sympy_integrate            | 19.8 ms                                                                                                           | 24.2 ms: 1.22x slower                                                                                                   |
| raytrace                   | 262 ms                                                                                                            | 323 ms: 1.23x slower                                                                                                    |
| connected_components       | 393 ms                                                                                                            | 485 ms: 1.24x slower                                                                                                    |
| tomli_loads                | 1.86 sec                                                                                                          | 2.30 sec: 1.24x slower                                                                                                  |
| deepcopy_reduce            | 2.62 us                                                                                                           | 3.24 us: 1.24x slower                                                                                                   |
| coverage                   | 79.1 ms                                                                                                           | 98.0 ms: 1.24x slower                                                                                                   |
| chaos                      | 54.6 ms                                                                                                           | 67.7 ms: 1.24x slower                                                                                                   |
| comprehensions             | 16.8 us                                                                                                           | 20.9 us: 1.24x slower                                                                                                   |
| nqueens                    | 77.5 ms                                                                                                           | 96.8 ms: 1.25x slower                                                                                                   |
| shortest_path              | 431 ms                                                                                                            | 539 ms: 1.25x slower                                                                                                    |
| genshi_xml                 | 48.2 ms                                                                                                           | 60.2 ms: 1.25x slower                                                                                                   |
| sqlglot_parse              | 1.25 ms                                                                                                           | 1.57 ms: 1.25x slower                                                                                                   |
| deepcopy_memo              | 30.2 us                                                                                                           | 37.9 us: 1.26x slower                                                                                                   |
| sqlalchemy_imperative      | 19.4 ms                                                                                                           | 24.4 ms: 1.26x slower                                                                                                   |
| scimark_monte_carlo        | 63.7 ms                                                                                                           | 80.6 ms: 1.27x slower                                                                                                   |
| typing_runtime_protocols   | 158 us                                                                                                            | 200 us: 1.27x slower                                                                                                    |
| sqlalchemy_declarative     | 128 ms                                                                                                            | 163 ms: 1.27x slower                                                                                                    |
| python_startup_no_site     | 7.47 ms                                                                                                           | 9.54 ms: 1.28x slower                                                                                                   |
| hexiom                     | 5.75 ms                                                                                                           | 7.36 ms: 1.28x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.27 ms                                                                                                           | 5.50 ms: 1.29x slower                                                                                                   |
| crypto_pyaes               | 67.5 ms                                                                                                           | 87.2 ms: 1.29x slower                                                                                                   |
| fannkuch                   | 363 ms                                                                                                            | 471 ms: 1.30x slower                                                                                                    |
| genshi_text                | 21.2 ms                                                                                                           | 27.5 ms: 1.30x slower                                                                                                   |
| meteor_contest             | 99.3 ms                                                                                                           | 131 ms: 1.32x slower                                                                                                    |
| richards                   | 41.7 ms                                                                                                           | 55.6 ms: 1.33x slower                                                                                                   |
| mako                       | 11.7 ms                                                                                                           | 15.6 ms: 1.33x slower                                                                                                   |
| richards_super             | 48.1 ms                                                                                                           | 64.7 ms: 1.35x slower                                                                                                   |
| deltablue                  | 3.16 ms                                                                                                           | 4.60 ms: 1.45x slower                                                                                                   |
| nbody                      | 86.5 ms                                                                                                           | 134 ms: 1.54x slower                                                                                                    |
| bench_thread_pool          | 1.04 ms                                                                                                           | 3.32 ms: 3.20x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: html5lib

- Geometric mean (including insignificant results): 1.126x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.21x