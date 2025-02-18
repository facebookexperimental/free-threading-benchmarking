# Results vs. base

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 438 ms                                                                                                            | 539 ms: 1.23x slower                                                                                                    |
| docutils       | 3.56 sec                                                                                                          | 4.09 sec: 1.15x slower                                                                                                  |
| html5lib       | 82.9 ms                                                                                                           | 95.3 ms: 1.15x slower                                                                                                   |
| sphinx         | 1.38 sec                                                                                                          | 1.64 sec: 1.19x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg         | 403 ms                                                                                                            | 349 ms: 1.16x faster                                                                                                    |
| async_tree_io_tg           | 919 ms                                                                                                            | 814 ms: 1.13x faster                                                                                                    |
| async_tree_io              | 931 ms                                                                                                            | 871 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 697 ms                                                                                                            | 668 ms: 1.04x faster                                                                                                    |
| async_generators           | 545 ms                                                                                                            | 564 ms: 1.03x slower                                                                                                    |
| coroutines                 | 29.7 ms                                                                                                           | 31.5 ms: 1.06x slower                                                                                                   |
| async_tree_memoization_tg  | 464 ms                                                                                                            | 496 ms: 1.07x slower                                                                                                    |
| async_tree_memoization     | 480 ms                                                                                                            | 547 ms: 1.14x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (3): async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 98.6 ms                                                                                                           | 104 ms: 1.06x slower                                                                                                    |
| pidigits       | 226 ms                                                                                                            | 245 ms: 1.08x slower                                                                                                    |
| nbody          | 124 ms                                                                                                            | 180 ms: 1.45x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 35.0 ms                                                                                                           | 33.5 ms: 1.05x faster                                                                                                   |
| regex_dna      | 279 ms                                                                                                            | 299 ms: 1.07x slower                                                                                                    |
| regex_effbot   | 4.20 ms                                                                                                           | 4.66 ms: 1.11x slower                                                                                                   |
| regex_compile  | 171 ms                                                                                                            | 199 ms: 1.17x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 150 ms                                                                                                            | 139 ms: 1.08x faster                                                                                                    |
| json_loads           | 40.3 us                                                                                                           | 41.8 us: 1.04x slower                                                                                                   |
| xml_etree_parse      | 201 ms                                                                                                            | 210 ms: 1.05x slower                                                                                                    |
| xml_etree_generate   | 121 ms                                                                                                            | 130 ms: 1.07x slower                                                                                                    |
| xml_etree_process    | 86.1 ms                                                                                                           | 95.8 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python | 303 us                                                                                                            | 346 us: 1.14x slower                                                                                                    |
| pickle_pure_python   | 403 us                                                                                                            | 483 us: 1.20x slower                                                                                                    |
| tomli_loads          | 2.53 sec                                                                                                          | 3.05 sec: 1.20x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 26.6 ms                                                                                                           | 31.7 ms: 1.19x slower                                                                                                   |
| python_startup_no_site | 15.6 ms                                                                                                           | 20.7 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 45.0 ms                                                                                                           | 53.0 ms: 1.18x slower                                                                                                   |
| genshi_xml      | 65.2 ms                                                                                                           | 79.3 ms: 1.22x slower                                                                                                   |
| mako            | 16.4 ms                                                                                                           | 22.2 ms: 1.35x slower                                                                                                   |
| genshi_text     | 27.8 ms                                                                                                           | 39.4 ms: 1.42x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.29x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json | results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 8.78 ms                                                                                                           | 3.28 ms: 2.67x faster                                                                                                   |
| create_gc_cycles           | 3.46 ms                                                                                                           | 2.44 ms: 1.42x faster                                                                                                   |
| async_tree_none_tg         | 403 ms                                                                                                            | 349 ms: 1.16x faster                                                                                                    |
| async_tree_io_tg           | 919 ms                                                                                                            | 814 ms: 1.13x faster                                                                                                    |
| bench_mp_pool              | 91.0 ms                                                                                                           | 84.3 ms: 1.08x faster                                                                                                   |
| xml_etree_iterparse        | 150 ms                                                                                                            | 139 ms: 1.08x faster                                                                                                    |
| async_tree_io              | 931 ms                                                                                                            | 871 ms: 1.07x faster                                                                                                    |
| sqlite_synth               | 3.81 us                                                                                                           | 3.64 us: 1.05x faster                                                                                                   |
| regex_v8                   | 35.0 ms                                                                                                           | 33.5 ms: 1.05x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                                                                            | 668 ms: 1.04x faster                                                                                                    |
| async_generators           | 545 ms                                                                                                            | 564 ms: 1.03x slower                                                                                                    |
| json_loads                 | 40.3 us                                                                                                           | 41.8 us: 1.04x slower                                                                                                   |
| xml_etree_parse            | 201 ms                                                                                                            | 210 ms: 1.05x slower                                                                                                    |
| pycparser                  | 1.58 sec                                                                                                          | 1.66 sec: 1.05x slower                                                                                                  |
| logging_silent             | 136 ns                                                                                                            | 143 ns: 1.05x slower                                                                                                    |
| float                      | 98.6 ms                                                                                                           | 104 ms: 1.06x slower                                                                                                    |
| k_core                     | 4.09 sec                                                                                                          | 4.33 sec: 1.06x slower                                                                                                  |
| coroutines                 | 29.7 ms                                                                                                           | 31.5 ms: 1.06x slower                                                                                                   |
| scimark_sor                | 158 ms                                                                                                            | 168 ms: 1.07x slower                                                                                                    |
| async_tree_memoization_tg  | 464 ms                                                                                                            | 496 ms: 1.07x slower                                                                                                    |
| xml_etree_generate         | 121 ms                                                                                                            | 130 ms: 1.07x slower                                                                                                    |
| regex_dna                  | 279 ms                                                                                                            | 299 ms: 1.07x slower                                                                                                    |
| dulwich_log                | 95.2 ms                                                                                                           | 103 ms: 1.08x slower                                                                                                    |
| json                       | 7.38 ms                                                                                                           | 7.97 ms: 1.08x slower                                                                                                   |
| pidigits                   | 226 ms                                                                                                            | 245 ms: 1.08x slower                                                                                                    |
| generators                 | 41.3 ms                                                                                                           | 45.3 ms: 1.10x slower                                                                                                   |
| deepcopy                   | 379 us                                                                                                            | 417 us: 1.10x slower                                                                                                    |
| logging_simple             | 8.56 us                                                                                                           | 9.46 us: 1.11x slower                                                                                                   |
| deepcopy_reduce            | 3.76 us                                                                                                           | 4.16 us: 1.11x slower                                                                                                   |
| regex_effbot               | 4.20 ms                                                                                                           | 4.66 ms: 1.11x slower                                                                                                   |
| xml_etree_process          | 86.1 ms                                                                                                           | 95.8 ms: 1.11x slower                                                                                                   |
| sqlglot_normalize          | 142 ms                                                                                                            | 159 ms: 1.11x slower                                                                                                    |
| telco                      | 10.5 ms                                                                                                           | 11.7 ms: 1.12x slower                                                                                                   |
| richards_super             | 71.2 ms                                                                                                           | 80.2 ms: 1.13x slower                                                                                                   |
| coverage                   | 124 ms                                                                                                            | 140 ms: 1.13x slower                                                                                                    |
| mdp                        | 3.58 sec                                                                                                          | 4.07 sec: 1.14x slower                                                                                                  |
| pyflate                    | 658 ms                                                                                                            | 748 ms: 1.14x slower                                                                                                    |
| async_tree_memoization     | 480 ms                                                                                                            | 547 ms: 1.14x slower                                                                                                    |
| unpickle_pure_python       | 303 us                                                                                                            | 346 us: 1.14x slower                                                                                                    |
| spectral_norm              | 121 ms                                                                                                            | 139 ms: 1.14x slower                                                                                                    |
| docutils                   | 3.56 sec                                                                                                          | 4.09 sec: 1.15x slower                                                                                                  |
| html5lib                   | 82.9 ms                                                                                                           | 95.3 ms: 1.15x slower                                                                                                   |
| regex_compile              | 171 ms                                                                                                            | 199 ms: 1.17x slower                                                                                                    |
| pprint_safe_repr           | 948 ms                                                                                                            | 1.11 sec: 1.17x slower                                                                                                  |
| django_template            | 45.0 ms                                                                                                           | 53.0 ms: 1.18x slower                                                                                                   |
| bpe_tokeniser              | 5.87 sec                                                                                                          | 6.92 sec: 1.18x slower                                                                                                  |
| pprint_pformat             | 1.94 sec                                                                                                          | 2.30 sec: 1.18x slower                                                                                                  |
| shortest_path              | 885 ms                                                                                                            | 1.05 sec: 1.18x slower                                                                                                  |
| sphinx                     | 1.38 sec                                                                                                          | 1.64 sec: 1.19x slower                                                                                                  |
| richards                   | 58.2 ms                                                                                                           | 69.4 ms: 1.19x slower                                                                                                   |
| python_startup             | 26.6 ms                                                                                                           | 31.7 ms: 1.19x slower                                                                                                   |
| sympy_sum                  | 204 ms                                                                                                            | 243 ms: 1.19x slower                                                                                                    |
| scimark_lu                 | 149 ms                                                                                                            | 179 ms: 1.19x slower                                                                                                    |
| pylint                     | 385 ms                                                                                                            | 461 ms: 1.20x slower                                                                                                    |
| hexiom                     | 8.49 ms                                                                                                           | 10.2 ms: 1.20x slower                                                                                                   |
| sympy_str                  | 350 ms                                                                                                            | 419 ms: 1.20x slower                                                                                                    |
| many_optionals             | 1.28 ms                                                                                                           | 1.53 ms: 1.20x slower                                                                                                   |
| pickle_pure_python         | 403 us                                                                                                            | 483 us: 1.20x slower                                                                                                    |
| connected_components       | 814 ms                                                                                                            | 978 ms: 1.20x slower                                                                                                    |
| sympy_integrate            | 27.8 ms                                                                                                           | 33.4 ms: 1.20x slower                                                                                                   |
| meteor_contest             | 148 ms                                                                                                            | 178 ms: 1.20x slower                                                                                                    |
| scimark_fft                | 442 ms                                                                                                            | 531 ms: 1.20x slower                                                                                                    |
| tomli_loads                | 2.53 sec                                                                                                          | 3.05 sec: 1.20x slower                                                                                                  |
| sympy_expand               | 599 ms                                                                                                            | 722 ms: 1.21x slower                                                                                                    |
| sqlalchemy_declarative     | 172 ms                                                                                                            | 207 ms: 1.21x slower                                                                                                    |
| genshi_xml                 | 65.2 ms                                                                                                           | 79.3 ms: 1.22x slower                                                                                                   |
| deepcopy_memo              | 41.3 us                                                                                                           | 50.5 us: 1.22x slower                                                                                                   |
| raytrace                   | 361 ms                                                                                                            | 441 ms: 1.22x slower                                                                                                    |
| crypto_pyaes               | 97.4 ms                                                                                                           | 119 ms: 1.23x slower                                                                                                    |
| 2to3                       | 438 ms                                                                                                            | 539 ms: 1.23x slower                                                                                                    |
| typing_runtime_protocols   | 216 us                                                                                                            | 268 us: 1.24x slower                                                                                                    |
| deltablue                  | 4.25 ms                                                                                                           | 5.27 ms: 1.24x slower                                                                                                   |
| chaos                      | 75.6 ms                                                                                                           | 94.2 ms: 1.25x slower                                                                                                   |
| sqlglot_parse              | 1.81 ms                                                                                                           | 2.25 ms: 1.25x slower                                                                                                   |
| nqueens                    | 105 ms                                                                                                            | 131 ms: 1.25x slower                                                                                                    |
| bench_thread_pool          | 3.13 ms                                                                                                           | 3.94 ms: 1.26x slower                                                                                                   |
| scimark_monte_carlo        | 88.2 ms                                                                                                           | 112 ms: 1.27x slower                                                                                                    |
| comprehensions             | 20.2 us                                                                                                           | 25.7 us: 1.27x slower                                                                                                   |
| go                         | 155 ms                                                                                                            | 200 ms: 1.29x slower                                                                                                    |
| thrift                     | 983 us                                                                                                            | 1.27 ms: 1.29x slower                                                                                                   |
| sqlalchemy_imperative      | 23.5 ms                                                                                                           | 31.0 ms: 1.32x slower                                                                                                   |
| fannkuch                   | 508 ms                                                                                                            | 673 ms: 1.32x slower                                                                                                    |
| python_startup_no_site     | 15.6 ms                                                                                                           | 20.7 ms: 1.33x slower                                                                                                   |
| sqlglot_transpile          | 2.06 ms                                                                                                           | 2.74 ms: 1.33x slower                                                                                                   |
| subparsers                 | 31.0 ms                                                                                                           | 41.6 ms: 1.34x slower                                                                                                   |
| logging_format             | 8.38 us                                                                                                           | 11.3 us: 1.34x slower                                                                                                   |
| mako                       | 16.4 ms                                                                                                           | 22.2 ms: 1.35x slower                                                                                                   |
| scimark_sparse_mat_mult    | 5.81 ms                                                                                                           | 8.06 ms: 1.39x slower                                                                                                   |
| genshi_text                | 27.8 ms                                                                                                           | 39.4 ms: 1.42x slower                                                                                                   |
| nbody                      | 124 ms                                                                                                            | 180 ms: 1.45x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (6): async_tree_none, asyncio_websockets, sqlglot_optimize, pathlib, json_dumps, async_tree_cpu_io_mixed

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.19x