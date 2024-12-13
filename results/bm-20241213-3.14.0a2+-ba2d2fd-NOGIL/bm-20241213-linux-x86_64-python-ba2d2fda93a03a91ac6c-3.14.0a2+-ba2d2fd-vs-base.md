# Results vs. base

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.243x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 435 ms                                                                                                            | 595 ms: 1.37x slower                                                                                                    |
| docutils       | 3.67 sec                                                                                                          | 4.43 sec: 1.21x slower                                                                                                  |
| html5lib       | 82.9 ms                                                                                                           | 124 ms: 1.49x slower                                                                                                    |
| sphinx         | 1.44 sec                                                                                                          | 1.75 sec: 1.21x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.31x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 31.0 ms                                                                                                           | 33.6 ms: 1.08x slower                                                                                                   |
| async_tree_none_tg         | 373 ms                                                                                                            | 440 ms: 1.18x slower                                                                                                    |
| async_generators           | 552 ms                                                                                                            | 653 ms: 1.18x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 674 ms                                                                                                            | 799 ms: 1.19x slower                                                                                                    |
| async_tree_io_tg           | 864 ms                                                                                                            | 1.06 sec: 1.23x slower                                                                                                  |
| async_tree_io              | 894 ms                                                                                                            | 1.14 sec: 1.27x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 662 ms                                                                                                            | 866 ms: 1.31x slower                                                                                                    |
| async_tree_none            | 387 ms                                                                                                            | 533 ms: 1.38x slower                                                                                                    |
| async_tree_memoization_tg  | 452 ms                                                                                                            | 634 ms: 1.40x slower                                                                                                    |
| async_tree_memoization     | 471 ms                                                                                                            | 683 ms: 1.45x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.24x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                                                                            | 181 ms: 1.43x slower                                                                                                    |
| float          | 111 ms                                                                                                            | 181 ms: 1.64x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.33x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 34.7 ms                                                                                                           | 33.3 ms: 1.04x faster                                                                                                   |
| regex_dna      | 271 ms                                                                                                            | 302 ms: 1.11x slower                                                                                                    |
| regex_compile  | 165 ms                                                                                                            | 231 ms: 1.40x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 145 ms                                                                                                            | 137 ms: 1.06x faster                                                                                                    |
| xml_etree_generate   | 123 ms                                                                                                            | 128 ms: 1.04x slower                                                                                                    |
| xml_etree_parse      | 196 ms                                                                                                            | 206 ms: 1.05x slower                                                                                                    |
| json_loads           | 33.8 us                                                                                                           | 38.3 us: 1.13x slower                                                                                                   |
| json_dumps           | 15.2 ms                                                                                                           | 18.1 ms: 1.19x slower                                                                                                   |
| xml_etree_process    | 83.4 ms                                                                                                           | 107 ms: 1.28x slower                                                                                                    |
| tomli_loads          | 2.72 sec                                                                                                          | 3.50 sec: 1.29x slower                                                                                                  |
| unpickle_pure_python | 274 us                                                                                                            | 406 us: 1.48x slower                                                                                                    |
| pickle_pure_python   | 437 us                                                                                                            | 664 us: 1.52x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 15.7 ms                                                                                                           | 20.8 ms: 1.32x slower                                                                                                   |
| python_startup         | 25.9 ms                                                                                                           | 34.6 ms: 1.34x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.33x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 67.9 ms                                                                                                           | 88.3 ms: 1.30x slower                                                                                                   |
| django_template | 45.3 ms                                                                                                           | 63.3 ms: 1.40x slower                                                                                                   |
| genshi_text     | 29.3 ms                                                                                                           | 42.1 ms: 1.43x slower                                                                                                   |
| mako            | 16.8 ms                                                                                                           | 27.5 ms: 1.63x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.44x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json | results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 8.42 ms                                                                                                           | 6.65 ms: 1.27x faster                                                                                                   |
| xml_etree_iterparse        | 145 ms                                                                                                            | 137 ms: 1.06x faster                                                                                                    |
| regex_v8                   | 34.7 ms                                                                                                           | 33.3 ms: 1.04x faster                                                                                                   |
| xml_etree_generate         | 123 ms                                                                                                            | 128 ms: 1.04x slower                                                                                                    |
| xml_etree_parse            | 196 ms                                                                                                            | 206 ms: 1.05x slower                                                                                                    |
| coroutines                 | 31.0 ms                                                                                                           | 33.6 ms: 1.08x slower                                                                                                   |
| json                       | 6.44 ms                                                                                                           | 7.00 ms: 1.09x slower                                                                                                   |
| k_core                     | 4.10 sec                                                                                                          | 4.49 sec: 1.09x slower                                                                                                  |
| regex_dna                  | 271 ms                                                                                                            | 302 ms: 1.11x slower                                                                                                    |
| json_loads                 | 33.8 us                                                                                                           | 38.3 us: 1.13x slower                                                                                                   |
| mdp                        | 3.91 sec                                                                                                          | 4.48 sec: 1.15x slower                                                                                                  |
| pathlib                    | 26.6 ms                                                                                                           | 30.6 ms: 1.15x slower                                                                                                   |
| shortest_path              | 874 ms                                                                                                            | 1.01 sec: 1.16x slower                                                                                                  |
| connected_components       | 807 ms                                                                                                            | 946 ms: 1.17x slower                                                                                                    |
| async_tree_none_tg         | 373 ms                                                                                                            | 440 ms: 1.18x slower                                                                                                    |
| async_generators           | 552 ms                                                                                                            | 653 ms: 1.18x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 674 ms                                                                                                            | 799 ms: 1.19x slower                                                                                                    |
| json_dumps                 | 15.2 ms                                                                                                           | 18.1 ms: 1.19x slower                                                                                                   |
| typing_runtime_protocols   | 227 us                                                                                                            | 272 us: 1.20x slower                                                                                                    |
| docutils                   | 3.67 sec                                                                                                          | 4.43 sec: 1.21x slower                                                                                                  |
| sphinx                     | 1.44 sec                                                                                                          | 1.75 sec: 1.21x slower                                                                                                  |
| spectral_norm              | 145 ms                                                                                                            | 176 ms: 1.21x slower                                                                                                    |
| many_optionals             | 1.13 ms                                                                                                           | 1.38 ms: 1.22x slower                                                                                                   |
| pycparser                  | 1.60 sec                                                                                                          | 1.97 sec: 1.23x slower                                                                                                  |
| async_tree_io_tg           | 864 ms                                                                                                            | 1.06 sec: 1.23x slower                                                                                                  |
| nqueens                    | 99.9 ms                                                                                                           | 123 ms: 1.23x slower                                                                                                    |
| scimark_fft                | 460 ms                                                                                                            | 574 ms: 1.25x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                                                                           | 7.85 ms: 1.25x slower                                                                                                   |
| deepcopy_reduce            | 3.62 us                                                                                                           | 4.54 us: 1.25x slower                                                                                                   |
| deepcopy_memo              | 40.6 us                                                                                                           | 50.9 us: 1.26x slower                                                                                                   |
| async_tree_io              | 894 ms                                                                                                            | 1.14 sec: 1.27x slower                                                                                                  |
| sqlglot_normalize          | 137 ms                                                                                                            | 174 ms: 1.27x slower                                                                                                    |
| bench_thread_pool          | 3.17 ms                                                                                                           | 4.04 ms: 1.27x slower                                                                                                   |
| xml_etree_process          | 83.4 ms                                                                                                           | 107 ms: 1.28x slower                                                                                                    |
| tomli_loads                | 2.72 sec                                                                                                          | 3.50 sec: 1.29x slower                                                                                                  |
| crypto_pyaes               | 95.2 ms                                                                                                           | 123 ms: 1.29x slower                                                                                                    |
| coverage                   | 108 ms                                                                                                            | 140 ms: 1.29x slower                                                                                                    |
| genshi_xml                 | 67.9 ms                                                                                                           | 88.3 ms: 1.30x slower                                                                                                   |
| fannkuch                   | 516 ms                                                                                                            | 672 ms: 1.30x slower                                                                                                    |
| sqlglot_optimize           | 69.8 ms                                                                                                           | 91.1 ms: 1.31x slower                                                                                                   |
| telco                      | 9.74 ms                                                                                                           | 12.7 ms: 1.31x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 662 ms                                                                                                            | 866 ms: 1.31x slower                                                                                                    |
| generators                 | 40.1 ms                                                                                                           | 52.9 ms: 1.32x slower                                                                                                   |
| deepcopy                   | 347 us                                                                                                            | 458 us: 1.32x slower                                                                                                    |
| python_startup_no_site     | 15.7 ms                                                                                                           | 20.8 ms: 1.32x slower                                                                                                   |
| pylint                     | 394 ms                                                                                                            | 524 ms: 1.33x slower                                                                                                    |
| python_startup             | 25.9 ms                                                                                                           | 34.6 ms: 1.34x slower                                                                                                   |
| bpe_tokeniser              | 5.82 sec                                                                                                          | 7.82 sec: 1.34x slower                                                                                                  |
| subparsers                 | 32.4 ms                                                                                                           | 43.7 ms: 1.35x slower                                                                                                   |
| meteor_contest             | 133 ms                                                                                                            | 180 ms: 1.35x slower                                                                                                    |
| 2to3                       | 435 ms                                                                                                            | 595 ms: 1.37x slower                                                                                                    |
| async_tree_none            | 387 ms                                                                                                            | 533 ms: 1.38x slower                                                                                                    |
| pprint_safe_repr           | 935 ms                                                                                                            | 1.29 sec: 1.38x slower                                                                                                  |
| pprint_pformat             | 1.90 sec                                                                                                          | 2.65 sec: 1.39x slower                                                                                                  |
| django_template            | 45.3 ms                                                                                                           | 63.3 ms: 1.40x slower                                                                                                   |
| regex_compile              | 165 ms                                                                                                            | 231 ms: 1.40x slower                                                                                                    |
| async_tree_memoization_tg  | 452 ms                                                                                                            | 634 ms: 1.40x slower                                                                                                    |
| scimark_lu                 | 156 ms                                                                                                            | 221 ms: 1.42x slower                                                                                                    |
| pyflate                    | 644 ms                                                                                                            | 916 ms: 1.42x slower                                                                                                    |
| thrift                     | 1.11 ms                                                                                                           | 1.58 ms: 1.42x slower                                                                                                   |
| nbody                      | 127 ms                                                                                                            | 181 ms: 1.43x slower                                                                                                    |
| genshi_text                | 29.3 ms                                                                                                           | 42.1 ms: 1.43x slower                                                                                                   |
| logging_simple             | 9.12 us                                                                                                           | 13.1 us: 1.44x slower                                                                                                   |
| async_tree_memoization     | 471 ms                                                                                                            | 683 ms: 1.45x slower                                                                                                    |
| sympy_integrate            | 27.3 ms                                                                                                           | 39.9 ms: 1.46x slower                                                                                                   |
| unpickle_pure_python       | 274 us                                                                                                            | 406 us: 1.48x slower                                                                                                    |
| richards                   | 61.0 ms                                                                                                           | 91.1 ms: 1.49x slower                                                                                                   |
| html5lib                   | 82.9 ms                                                                                                           | 124 ms: 1.49x slower                                                                                                    |
| logging_format             | 9.34 us                                                                                                           | 14.0 us: 1.49x slower                                                                                                   |
| chaos                      | 80.9 ms                                                                                                           | 121 ms: 1.50x slower                                                                                                    |
| logging_silent             | 144 ns                                                                                                            | 218 ns: 1.52x slower                                                                                                    |
| pickle_pure_python         | 437 us                                                                                                            | 664 us: 1.52x slower                                                                                                    |
| comprehensions             | 22.4 us                                                                                                           | 34.1 us: 1.52x slower                                                                                                   |
| sqlalchemy_declarative     | 173 ms                                                                                                            | 267 ms: 1.54x slower                                                                                                    |
| richards_super             | 67.3 ms                                                                                                           | 104 ms: 1.54x slower                                                                                                    |
| scimark_monte_carlo        | 89.1 ms                                                                                                           | 143 ms: 1.60x slower                                                                                                    |
| sympy_str                  | 373 ms                                                                                                            | 598 ms: 1.60x slower                                                                                                    |
| hexiom                     | 8.24 ms                                                                                                           | 13.3 ms: 1.61x slower                                                                                                   |
| mako                       | 16.8 ms                                                                                                           | 27.5 ms: 1.63x slower                                                                                                   |
| float                      | 111 ms                                                                                                            | 181 ms: 1.64x slower                                                                                                    |
| sqlglot_transpile          | 2.26 ms                                                                                                           | 3.79 ms: 1.68x slower                                                                                                   |
| sqlalchemy_imperative      | 21.2 ms                                                                                                           | 37.3 ms: 1.76x slower                                                                                                   |
| scimark_sor                | 163 ms                                                                                                            | 297 ms: 1.82x slower                                                                                                    |
| sqlglot_parse              | 1.77 ms                                                                                                           | 3.25 ms: 1.83x slower                                                                                                   |
| raytrace                   | 347 ms                                                                                                            | 645 ms: 1.86x slower                                                                                                    |
| go                         | 160 ms                                                                                                            | 314 ms: 1.96x slower                                                                                                    |
| sympy_expand               | 590 ms                                                                                                            | 1.16 sec: 1.97x slower                                                                                                  |
| sympy_sum                  | 214 ms                                                                                                            | 424 ms: 1.98x slower                                                                                                    |
| deltablue                  | 4.62 ms                                                                                                           | 11.1 ms: 2.41x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.32x slower                                                                                                            |

Benchmark hidden because not significant (7): create_gc_cycles, regex_effbot, asyncio_websockets, pidigits, dulwich_log, sqlite_synth, bench_mp_pool

- Geometric mean (including insignificant results): 1.243x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x