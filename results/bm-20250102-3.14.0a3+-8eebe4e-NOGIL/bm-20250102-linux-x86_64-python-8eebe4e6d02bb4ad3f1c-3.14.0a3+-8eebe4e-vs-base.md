# Results vs. base

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.225x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 410 ms                                                                                                            | 602 ms: 1.47x slower                                                                                                    |
| docutils       | 3.51 sec                                                                                                          | 4.33 sec: 1.23x slower                                                                                                  |
| html5lib       | 81.3 ms                                                                                                           | 120 ms: 1.48x slower                                                                                                    |
| sphinx         | 1.42 sec                                                                                                          | 1.74 sec: 1.23x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.35x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 707 ms                                                                                                            | 755 ms: 1.07x slower                                                                                                    |
| coroutines                 | 29.8 ms                                                                                                           | 33.0 ms: 1.11x slower                                                                                                   |
| async_tree_io_tg           | 820 ms                                                                                                            | 918 ms: 1.12x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 643 ms                                                                                                            | 738 ms: 1.15x slower                                                                                                    |
| async_tree_io              | 838 ms                                                                                                            | 989 ms: 1.18x slower                                                                                                    |
| async_generators           | 538 ms                                                                                                            | 642 ms: 1.19x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 683 ms                                                                                                            | 834 ms: 1.22x slower                                                                                                    |
| async_tree_none_tg         | 336 ms                                                                                                            | 410 ms: 1.22x slower                                                                                                    |
| async_tree_none            | 383 ms                                                                                                            | 493 ms: 1.29x slower                                                                                                    |
| async_tree_memoization     | 466 ms                                                                                                            | 601 ms: 1.29x slower                                                                                                    |
| async_tree_memoization_tg  | 432 ms                                                                                                            | 567 ms: 1.31x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 231 ms                                                                                                            | 242 ms: 1.05x slower                                                                                                    |
| float          | 100 ms                                                                                                            | 142 ms: 1.41x slower                                                                                                    |
| nbody          | 120 ms                                                                                                            | 170 ms: 1.43x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.17 ms                                                                                                           | 4.55 ms: 1.09x slower                                                                                                   |
| regex_dna      | 268 ms                                                                                                            | 293 ms: 1.09x slower                                                                                                    |
| regex_compile  | 161 ms                                                                                                            | 211 ms: 1.32x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 147 ms                                                                                                            | 128 ms: 1.15x faster                                                                                                    |
| json_dumps           | 14.6 ms                                                                                                           | 17.1 ms: 1.18x slower                                                                                                   |
| json_loads           | 33.5 us                                                                                                           | 39.5 us: 1.18x slower                                                                                                   |
| xml_etree_generate   | 109 ms                                                                                                            | 131 ms: 1.20x slower                                                                                                    |
| tomli_loads          | 2.61 sec                                                                                                          | 3.27 sec: 1.25x slower                                                                                                  |
| xml_etree_process    | 78.3 ms                                                                                                           | 106 ms: 1.35x slower                                                                                                    |
| unpickle_pure_python | 288 us                                                                                                            | 416 us: 1.44x slower                                                                                                    |
| pickle_pure_python   | 425 us                                                                                                            | 614 us: 1.44x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 23.3 ms                                                                                                           | 30.4 ms: 1.31x slower                                                                                                   |
| python_startup_no_site | 14.7 ms                                                                                                           | 19.6 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.32x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 60.0 ms                                                                                                           | 85.7 ms: 1.43x slower                                                                                                   |
| genshi_text     | 28.3 ms                                                                                                           | 42.0 ms: 1.49x slower                                                                                                   |
| django_template | 43.6 ms                                                                                                           | 65.0 ms: 1.49x slower                                                                                                   |
| mako            | 16.0 ms                                                                                                           | 27.2 ms: 1.71x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.52x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json | results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.96 ms                                                                                                           | 6.06 ms: 1.31x faster                                                                                                   |
| xml_etree_iterparse        | 147 ms                                                                                                            | 128 ms: 1.15x faster                                                                                                    |
| create_gc_cycles           | 3.57 ms                                                                                                           | 3.32 ms: 1.07x faster                                                                                                   |
| sqlite_synth               | 3.57 us                                                                                                           | 3.71 us: 1.04x slower                                                                                                   |
| pidigits                   | 231 ms                                                                                                            | 242 ms: 1.05x slower                                                                                                    |
| asyncio_websockets         | 707 ms                                                                                                            | 755 ms: 1.07x slower                                                                                                    |
| k_core                     | 3.99 sec                                                                                                          | 4.29 sec: 1.08x slower                                                                                                  |
| regex_effbot               | 4.17 ms                                                                                                           | 4.55 ms: 1.09x slower                                                                                                   |
| regex_dna                  | 268 ms                                                                                                            | 293 ms: 1.09x slower                                                                                                    |
| telco                      | 10.5 ms                                                                                                           | 11.5 ms: 1.09x slower                                                                                                   |
| coroutines                 | 29.8 ms                                                                                                           | 33.0 ms: 1.11x slower                                                                                                   |
| async_tree_io_tg           | 820 ms                                                                                                            | 918 ms: 1.12x slower                                                                                                    |
| pathlib                    | 26.2 ms                                                                                                           | 29.9 ms: 1.14x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 643 ms                                                                                                            | 738 ms: 1.15x slower                                                                                                    |
| scimark_fft                | 451 ms                                                                                                            | 522 ms: 1.16x slower                                                                                                    |
| pycparser                  | 1.58 sec                                                                                                          | 1.84 sec: 1.17x slower                                                                                                  |
| sympy_sum                  | 208 ms                                                                                                            | 244 ms: 1.17x slower                                                                                                    |
| json_dumps                 | 14.6 ms                                                                                                           | 17.1 ms: 1.18x slower                                                                                                   |
| json_loads                 | 33.5 us                                                                                                           | 39.5 us: 1.18x slower                                                                                                   |
| async_tree_io              | 838 ms                                                                                                            | 989 ms: 1.18x slower                                                                                                    |
| json                       | 5.97 ms                                                                                                           | 7.05 ms: 1.18x slower                                                                                                   |
| async_generators           | 538 ms                                                                                                            | 642 ms: 1.19x slower                                                                                                    |
| connected_components       | 756 ms                                                                                                            | 908 ms: 1.20x slower                                                                                                    |
| dulwich_log                | 94.2 ms                                                                                                           | 113 ms: 1.20x slower                                                                                                    |
| xml_etree_generate         | 109 ms                                                                                                            | 131 ms: 1.20x slower                                                                                                    |
| spectral_norm              | 133 ms                                                                                                            | 161 ms: 1.21x slower                                                                                                    |
| sympy_str                  | 364 ms                                                                                                            | 443 ms: 1.22x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 683 ms                                                                                                            | 834 ms: 1.22x slower                                                                                                    |
| async_tree_none_tg         | 336 ms                                                                                                            | 410 ms: 1.22x slower                                                                                                    |
| sqlglot_normalize          | 138 ms                                                                                                            | 169 ms: 1.22x slower                                                                                                    |
| sphinx                     | 1.42 sec                                                                                                          | 1.74 sec: 1.23x slower                                                                                                  |
| sympy_expand               | 583 ms                                                                                                            | 717 ms: 1.23x slower                                                                                                    |
| docutils                   | 3.51 sec                                                                                                          | 4.33 sec: 1.23x slower                                                                                                  |
| mdp                        | 3.50 sec                                                                                                          | 4.33 sec: 1.24x slower                                                                                                  |
| coverage                   | 110 ms                                                                                                            | 137 ms: 1.24x slower                                                                                                    |
| nqueens                    | 103 ms                                                                                                            | 129 ms: 1.25x slower                                                                                                    |
| shortest_path              | 833 ms                                                                                                            | 1.04 sec: 1.25x slower                                                                                                  |
| sqlglot_optimize           | 71.3 ms                                                                                                           | 89.1 ms: 1.25x slower                                                                                                   |
| tomli_loads                | 2.61 sec                                                                                                          | 3.27 sec: 1.25x slower                                                                                                  |
| fannkuch                   | 517 ms                                                                                                            | 654 ms: 1.27x slower                                                                                                    |
| meteor_contest             | 139 ms                                                                                                            | 177 ms: 1.27x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.42 ms                                                                                                           | 8.15 ms: 1.27x slower                                                                                                   |
| pylint                     | 378 ms                                                                                                            | 480 ms: 1.27x slower                                                                                                    |
| crypto_pyaes               | 96.1 ms                                                                                                           | 122 ms: 1.27x slower                                                                                                    |
| sympy_integrate            | 27.3 ms                                                                                                           | 35.0 ms: 1.28x slower                                                                                                   |
| async_tree_none            | 383 ms                                                                                                            | 493 ms: 1.29x slower                                                                                                    |
| async_tree_memoization     | 466 ms                                                                                                            | 601 ms: 1.29x slower                                                                                                    |
| deepcopy                   | 321 us                                                                                                            | 414 us: 1.29x slower                                                                                                    |
| thrift                     | 984 us                                                                                                            | 1.29 ms: 1.31x slower                                                                                                   |
| python_startup             | 23.3 ms                                                                                                           | 30.4 ms: 1.31x slower                                                                                                   |
| scimark_lu                 | 149 ms                                                                                                            | 195 ms: 1.31x slower                                                                                                    |
| async_tree_memoization_tg  | 432 ms                                                                                                            | 567 ms: 1.31x slower                                                                                                    |
| regex_compile              | 161 ms                                                                                                            | 211 ms: 1.32x slower                                                                                                    |
| typing_runtime_protocols   | 206 us                                                                                                            | 272 us: 1.32x slower                                                                                                    |
| richards_super             | 65.0 ms                                                                                                           | 85.9 ms: 1.32x slower                                                                                                   |
| deepcopy_reduce            | 3.35 us                                                                                                           | 4.43 us: 1.32x slower                                                                                                   |
| logging_format             | 9.41 us                                                                                                           | 12.5 us: 1.33x slower                                                                                                   |
| python_startup_no_site     | 14.7 ms                                                                                                           | 19.6 ms: 1.33x slower                                                                                                   |
| xml_etree_process          | 78.3 ms                                                                                                           | 106 ms: 1.35x slower                                                                                                    |
| richards                   | 57.8 ms                                                                                                           | 78.8 ms: 1.36x slower                                                                                                   |
| pprint_safe_repr           | 908 ms                                                                                                            | 1.24 sec: 1.36x slower                                                                                                  |
| bpe_tokeniser              | 5.75 sec                                                                                                          | 7.88 sec: 1.37x slower                                                                                                  |
| sqlalchemy_declarative     | 179 ms                                                                                                            | 245 ms: 1.37x slower                                                                                                    |
| pprint_pformat             | 1.82 sec                                                                                                          | 2.56 sec: 1.40x slower                                                                                                  |
| hexiom                     | 8.50 ms                                                                                                           | 12.0 ms: 1.41x slower                                                                                                   |
| float                      | 100 ms                                                                                                            | 142 ms: 1.41x slower                                                                                                    |
| deepcopy_memo              | 37.1 us                                                                                                           | 52.6 us: 1.42x slower                                                                                                   |
| nbody                      | 120 ms                                                                                                            | 170 ms: 1.43x slower                                                                                                    |
| genshi_xml                 | 60.0 ms                                                                                                           | 85.7 ms: 1.43x slower                                                                                                   |
| generators                 | 38.1 ms                                                                                                           | 54.5 ms: 1.43x slower                                                                                                   |
| unpickle_pure_python       | 288 us                                                                                                            | 416 us: 1.44x slower                                                                                                    |
| pickle_pure_python         | 425 us                                                                                                            | 614 us: 1.44x slower                                                                                                    |
| subparsers                 | 28.2 ms                                                                                                           | 41.1 ms: 1.46x slower                                                                                                   |
| pyflate                    | 621 ms                                                                                                            | 905 ms: 1.46x slower                                                                                                    |
| 2to3                       | 410 ms                                                                                                            | 602 ms: 1.47x slower                                                                                                    |
| bench_thread_pool          | 2.94 ms                                                                                                           | 4.33 ms: 1.47x slower                                                                                                   |
| sqlalchemy_imperative      | 23.1 ms                                                                                                           | 34.0 ms: 1.47x slower                                                                                                   |
| logging_simple             | 8.15 us                                                                                                           | 12.0 us: 1.48x slower                                                                                                   |
| html5lib                   | 81.3 ms                                                                                                           | 120 ms: 1.48x slower                                                                                                    |
| genshi_text                | 28.3 ms                                                                                                           | 42.0 ms: 1.49x slower                                                                                                   |
| django_template            | 43.6 ms                                                                                                           | 65.0 ms: 1.49x slower                                                                                                   |
| many_optionals             | 1.04 ms                                                                                                           | 1.57 ms: 1.51x slower                                                                                                   |
| comprehensions             | 21.4 us                                                                                                           | 33.6 us: 1.57x slower                                                                                                   |
| chaos                      | 77.2 ms                                                                                                           | 122 ms: 1.58x slower                                                                                                    |
| scimark_monte_carlo        | 86.3 ms                                                                                                           | 138 ms: 1.60x slower                                                                                                    |
| sqlglot_parse              | 1.80 ms                                                                                                           | 3.03 ms: 1.68x slower                                                                                                   |
| sqlglot_transpile          | 2.03 ms                                                                                                           | 3.43 ms: 1.69x slower                                                                                                   |
| mako                       | 16.0 ms                                                                                                           | 27.2 ms: 1.71x slower                                                                                                   |
| scimark_sor                | 160 ms                                                                                                            | 275 ms: 1.72x slower                                                                                                    |
| logging_silent             | 134 ns                                                                                                            | 230 ns: 1.72x slower                                                                                                    |
| raytrace                   | 336 ms                                                                                                            | 584 ms: 1.74x slower                                                                                                    |
| go                         | 157 ms                                                                                                            | 288 ms: 1.83x slower                                                                                                    |
| deltablue                  | 4.13 ms                                                                                                           | 10.4 ms: 2.53x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmark hidden because not significant (3): xml_etree_parse, regex_v8, bench_mp_pool

- Geometric mean (including insignificant results): 1.225x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.18x