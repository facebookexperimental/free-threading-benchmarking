# Results vs. base

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.277x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 448 ms                                                                                                            | 649 ms: 1.45x slower                                                                                                    |
| docutils       | 3.56 sec                                                                                                          | 4.44 sec: 1.24x slower                                                                                                  |
| html5lib       | 83.4 ms                                                                                                           | 124 ms: 1.49x slower                                                                                                    |
| sphinx         | 1.44 sec                                                                                                          | 1.74 sec: 1.21x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.34x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 879 ms                                                                                                            | 1.10 sec: 1.25x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 680 ms                                                                                                            | 853 ms: 1.26x slower                                                                                                    |
| coroutines                 | 30.5 ms                                                                                                           | 38.6 ms: 1.27x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 682 ms                                                                                                            | 867 ms: 1.27x slower                                                                                                    |
| async_generators           | 546 ms                                                                                                            | 709 ms: 1.30x slower                                                                                                    |
| async_tree_none            | 426 ms                                                                                                            | 559 ms: 1.31x slower                                                                                                    |
| async_tree_memoization_tg  | 469 ms                                                                                                            | 615 ms: 1.31x slower                                                                                                    |
| async_tree_none_tg         | 355 ms                                                                                                            | 488 ms: 1.37x slower                                                                                                    |
| async_tree_memoization     | 483 ms                                                                                                            | 681 ms: 1.41x slower                                                                                                    |
| async_tree_io              | 864 ms                                                                                                            | 1.25 sec: 1.45x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 234 ms                                                                                                            | 242 ms: 1.03x slower                                                                                                    |
| nbody          | 122 ms                                                                                                            | 195 ms: 1.60x slower                                                                                                    |
| float          | 108 ms                                                                                                            | 177 ms: 1.63x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.39x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 268 ms                                                                                                            | 305 ms: 1.14x slower                                                                                                    |
| regex_compile  | 180 ms                                                                                                            | 244 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 163 ms                                                                                                            | 134 ms: 1.21x faster                                                                                                    |
| json_loads           | 33.5 us                                                                                                           | 36.8 us: 1.10x slower                                                                                                   |
| json_dumps           | 15.3 ms                                                                                                           | 18.9 ms: 1.24x slower                                                                                                   |
| xml_etree_generate   | 114 ms                                                                                                            | 148 ms: 1.30x slower                                                                                                    |
| tomli_loads          | 2.71 sec                                                                                                          | 3.57 sec: 1.32x slower                                                                                                  |
| xml_etree_process    | 80.3 ms                                                                                                           | 106 ms: 1.32x slower                                                                                                    |
| pickle_pure_python   | 438 us                                                                                                            | 686 us: 1.56x slower                                                                                                    |
| unpickle_pure_python | 285 us                                                                                                            | 476 us: 1.67x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.23x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 23.9 ms                                                                                                           | 32.7 ms: 1.37x slower                                                                                                   |
| python_startup_no_site | 14.4 ms                                                                                                           | 20.3 ms: 1.41x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.39x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 28.8 ms                                                                                                           | 43.4 ms: 1.51x slower                                                                                                   |
| genshi_xml      | 65.9 ms                                                                                                           | 101 ms: 1.53x slower                                                                                                    |
| django_template | 46.1 ms                                                                                                           | 71.0 ms: 1.54x slower                                                                                                   |
| mako            | 16.3 ms                                                                                                           | 27.7 ms: 1.69x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.57x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json | results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse        | 163 ms                                                                                                            | 134 ms: 1.21x faster                                                                                                    |
| gc_traversal               | 7.02 ms                                                                                                           | 5.93 ms: 1.18x faster                                                                                                   |
| sqlite_synth               | 4.04 us                                                                                                           | 3.76 us: 1.07x faster                                                                                                   |
| pidigits                   | 234 ms                                                                                                            | 242 ms: 1.03x slower                                                                                                    |
| json_loads                 | 33.5 us                                                                                                           | 36.8 us: 1.10x slower                                                                                                   |
| pathlib                    | 27.1 ms                                                                                                           | 29.9 ms: 1.10x slower                                                                                                   |
| scimark_fft                | 479 ms                                                                                                            | 539 ms: 1.12x slower                                                                                                    |
| k_core                     | 3.96 sec                                                                                                          | 4.46 sec: 1.13x slower                                                                                                  |
| regex_dna                  | 268 ms                                                                                                            | 305 ms: 1.14x slower                                                                                                    |
| spectral_norm              | 154 ms                                                                                                            | 179 ms: 1.16x slower                                                                                                    |
| json                       | 6.19 ms                                                                                                           | 7.26 ms: 1.17x slower                                                                                                   |
| bench_mp_pool              | 88.9 ms                                                                                                           | 105 ms: 1.18x slower                                                                                                    |
| sqlglot_normalize          | 168 ms                                                                                                            | 198 ms: 1.18x slower                                                                                                    |
| meteor_contest             | 144 ms                                                                                                            | 174 ms: 1.21x slower                                                                                                    |
| sphinx                     | 1.44 sec                                                                                                          | 1.74 sec: 1.21x slower                                                                                                  |
| crypto_pyaes               | 98.4 ms                                                                                                           | 120 ms: 1.22x slower                                                                                                    |
| connected_components       | 779 ms                                                                                                            | 963 ms: 1.24x slower                                                                                                    |
| json_dumps                 | 15.3 ms                                                                                                           | 18.9 ms: 1.24x slower                                                                                                   |
| docutils                   | 3.56 sec                                                                                                          | 4.44 sec: 1.24x slower                                                                                                  |
| nqueens                    | 102 ms                                                                                                            | 127 ms: 1.25x slower                                                                                                    |
| async_tree_io_tg           | 879 ms                                                                                                            | 1.10 sec: 1.25x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 680 ms                                                                                                            | 853 ms: 1.26x slower                                                                                                    |
| shortest_path              | 856 ms                                                                                                            | 1.08 sec: 1.26x slower                                                                                                  |
| dulwich_log                | 94.4 ms                                                                                                           | 119 ms: 1.26x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.41 ms                                                                                                           | 8.09 ms: 1.26x slower                                                                                                   |
| coroutines                 | 30.5 ms                                                                                                           | 38.6 ms: 1.27x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 682 ms                                                                                                            | 867 ms: 1.27x slower                                                                                                    |
| deepcopy                   | 344 us                                                                                                            | 438 us: 1.27x slower                                                                                                    |
| telco                      | 10.2 ms                                                                                                           | 13.1 ms: 1.29x slower                                                                                                   |
| async_generators           | 546 ms                                                                                                            | 709 ms: 1.30x slower                                                                                                    |
| xml_etree_generate         | 114 ms                                                                                                            | 148 ms: 1.30x slower                                                                                                    |
| deepcopy_reduce            | 3.58 us                                                                                                           | 4.66 us: 1.30x slower                                                                                                   |
| pycparser                  | 1.57 sec                                                                                                          | 2.04 sec: 1.30x slower                                                                                                  |
| fannkuch                   | 528 ms                                                                                                            | 687 ms: 1.30x slower                                                                                                    |
| async_tree_none            | 426 ms                                                                                                            | 559 ms: 1.31x slower                                                                                                    |
| async_tree_memoization_tg  | 469 ms                                                                                                            | 615 ms: 1.31x slower                                                                                                    |
| tomli_loads                | 2.71 sec                                                                                                          | 3.57 sec: 1.32x slower                                                                                                  |
| subparsers                 | 34.8 ms                                                                                                           | 45.9 ms: 1.32x slower                                                                                                   |
| xml_etree_process          | 80.3 ms                                                                                                           | 106 ms: 1.32x slower                                                                                                    |
| bench_thread_pool          | 2.83 ms                                                                                                           | 3.76 ms: 1.33x slower                                                                                                   |
| many_optionals             | 1.21 ms                                                                                                           | 1.64 ms: 1.36x slower                                                                                                   |
| typing_runtime_protocols   | 221 us                                                                                                            | 300 us: 1.36x slower                                                                                                    |
| regex_compile              | 180 ms                                                                                                            | 244 ms: 1.36x slower                                                                                                    |
| mdp                        | 3.42 sec                                                                                                          | 4.65 sec: 1.36x slower                                                                                                  |
| python_startup             | 23.9 ms                                                                                                           | 32.7 ms: 1.37x slower                                                                                                   |
| async_tree_none_tg         | 355 ms                                                                                                            | 488 ms: 1.37x slower                                                                                                    |
| generators                 | 39.2 ms                                                                                                           | 54.0 ms: 1.37x slower                                                                                                   |
| async_tree_memoization     | 483 ms                                                                                                            | 681 ms: 1.41x slower                                                                                                    |
| python_startup_no_site     | 14.4 ms                                                                                                           | 20.3 ms: 1.41x slower                                                                                                   |
| sympy_integrate            | 28.8 ms                                                                                                           | 40.7 ms: 1.41x slower                                                                                                   |
| pylint                     | 393 ms                                                                                                            | 561 ms: 1.43x slower                                                                                                    |
| async_tree_io              | 864 ms                                                                                                            | 1.25 sec: 1.45x slower                                                                                                  |
| bpe_tokeniser              | 5.68 sec                                                                                                          | 8.23 sec: 1.45x slower                                                                                                  |
| 2to3                       | 448 ms                                                                                                            | 649 ms: 1.45x slower                                                                                                    |
| thrift                     | 1.03 ms                                                                                                           | 1.49 ms: 1.45x slower                                                                                                   |
| coverage                   | 102 ms                                                                                                            | 148 ms: 1.45x slower                                                                                                    |
| sqlglot_optimize           | 66.4 ms                                                                                                           | 96.8 ms: 1.46x slower                                                                                                   |
| pprint_safe_repr           | 920 ms                                                                                                            | 1.34 sec: 1.46x slower                                                                                                  |
| pyflate                    | 656 ms                                                                                                            | 967 ms: 1.47x slower                                                                                                    |
| deepcopy_memo              | 40.0 us                                                                                                           | 59.4 us: 1.49x slower                                                                                                   |
| html5lib                   | 83.4 ms                                                                                                           | 124 ms: 1.49x slower                                                                                                    |
| genshi_text                | 28.8 ms                                                                                                           | 43.4 ms: 1.51x slower                                                                                                   |
| pprint_pformat             | 1.86 sec                                                                                                          | 2.84 sec: 1.53x slower                                                                                                  |
| genshi_xml                 | 65.9 ms                                                                                                           | 101 ms: 1.53x slower                                                                                                    |
| django_template            | 46.1 ms                                                                                                           | 71.0 ms: 1.54x slower                                                                                                   |
| pickle_pure_python         | 438 us                                                                                                            | 686 us: 1.56x slower                                                                                                    |
| nbody                      | 122 ms                                                                                                            | 195 ms: 1.60x slower                                                                                                    |
| scimark_lu                 | 151 ms                                                                                                            | 244 ms: 1.62x slower                                                                                                    |
| float                      | 108 ms                                                                                                            | 177 ms: 1.63x slower                                                                                                    |
| richards                   | 62.9 ms                                                                                                           | 103 ms: 1.63x slower                                                                                                    |
| richards_super             | 69.6 ms                                                                                                           | 115 ms: 1.65x slower                                                                                                    |
| comprehensions             | 21.9 us                                                                                                           | 36.0 us: 1.65x slower                                                                                                   |
| scimark_monte_carlo        | 89.1 ms                                                                                                           | 148 ms: 1.66x slower                                                                                                    |
| unpickle_pure_python       | 285 us                                                                                                            | 476 us: 1.67x slower                                                                                                    |
| sympy_str                  | 367 ms                                                                                                            | 617 ms: 1.68x slower                                                                                                    |
| mako                       | 16.3 ms                                                                                                           | 27.7 ms: 1.69x slower                                                                                                   |
| logging_silent             | 139 ns                                                                                                            | 241 ns: 1.74x slower                                                                                                    |
| hexiom                     | 8.57 ms                                                                                                           | 15.4 ms: 1.80x slower                                                                                                   |
| sqlalchemy_declarative     | 163 ms                                                                                                            | 296 ms: 1.81x slower                                                                                                    |
| logging_simple             | 7.91 us                                                                                                           | 14.4 us: 1.82x slower                                                                                                   |
| chaos                      | 79.8 ms                                                                                                           | 150 ms: 1.88x slower                                                                                                    |
| sqlglot_parse              | 1.74 ms                                                                                                           | 3.28 ms: 1.88x slower                                                                                                   |
| sqlalchemy_imperative      | 21.6 ms                                                                                                           | 41.1 ms: 1.90x slower                                                                                                   |
| logging_format             | 8.29 us                                                                                                           | 16.1 us: 1.94x slower                                                                                                   |
| scimark_sor                | 158 ms                                                                                                            | 308 ms: 1.95x slower                                                                                                    |
| sqlglot_transpile          | 2.22 ms                                                                                                           | 4.42 ms: 1.99x slower                                                                                                   |
| raytrace                   | 348 ms                                                                                                            | 702 ms: 2.01x slower                                                                                                    |
| sympy_expand               | 602 ms                                                                                                            | 1.23 sec: 2.04x slower                                                                                                  |
| go                         | 154 ms                                                                                                            | 325 ms: 2.12x slower                                                                                                    |
| sympy_sum                  | 197 ms                                                                                                            | 452 ms: 2.29x slower                                                                                                    |
| deltablue                  | 4.30 ms                                                                                                           | 11.1 ms: 2.59x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.40x slower                                                                                                            |

Benchmark hidden because not significant (5): xml_etree_parse, asyncio_websockets, create_gc_cycles, regex_effbot, regex_v8

- Geometric mean (including insignificant results): 1.277x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.18x