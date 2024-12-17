# Results vs. base

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.240x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 429 ms                                                                                                            | 583 ms: 1.36x slower                                                                                                    |
| docutils       | 3.63 sec                                                                                                          | 4.37 sec: 1.20x slower                                                                                                  |
| html5lib       | 83.6 ms                                                                                                           | 123 ms: 1.47x slower                                                                                                    |
| sphinx         | 1.41 sec                                                                                                          | 1.65 sec: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 869 ms                                                                                                            | 1.01 sec: 1.17x slower                                                                                                  |
| async_tree_none_tg         | 378 ms                                                                                                            | 444 ms: 1.17x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 703 ms                                                                                                            | 828 ms: 1.18x slower                                                                                                    |
| coroutines                 | 29.5 ms                                                                                                           | 35.3 ms: 1.19x slower                                                                                                   |
| async_tree_io              | 877 ms                                                                                                            | 1.05 sec: 1.20x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 673 ms                                                                                                            | 810 ms: 1.20x slower                                                                                                    |
| async_generators           | 534 ms                                                                                                            | 651 ms: 1.22x slower                                                                                                    |
| async_tree_memoization     | 516 ms                                                                                                            | 641 ms: 1.24x slower                                                                                                    |
| async_tree_memoization_tg  | 460 ms                                                                                                            | 572 ms: 1.24x slower                                                                                                    |
| async_tree_none            | 401 ms                                                                                                            | 521 ms: 1.30x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 124 ms                                                                                                            | 173 ms: 1.40x slower                                                                                                    |
| float          | 108 ms                                                                                                            | 167 ms: 1.55x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.60 ms                                                                                                           | 4.09 ms: 1.13x faster                                                                                                   |
| regex_dna      | 277 ms                                                                                                            | 290 ms: 1.05x slower                                                                                                    |
| regex_compile  | 171 ms                                                                                                            | 214 ms: 1.25x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 146 ms                                                                                                            | 137 ms: 1.06x faster                                                                                                    |
| json_loads           | 34.4 us                                                                                                           | 36.0 us: 1.05x slower                                                                                                   |
| xml_etree_parse      | 193 ms                                                                                                            | 205 ms: 1.06x slower                                                                                                    |
| json_dumps           | 15.7 ms                                                                                                           | 17.5 ms: 1.12x slower                                                                                                   |
| xml_etree_generate   | 121 ms                                                                                                            | 137 ms: 1.13x slower                                                                                                    |
| tomli_loads          | 2.68 sec                                                                                                          | 3.31 sec: 1.23x slower                                                                                                  |
| xml_etree_process    | 78.9 ms                                                                                                           | 103 ms: 1.30x slower                                                                                                    |
| unpickle_pure_python | 290 us                                                                                                            | 414 us: 1.42x slower                                                                                                    |
| pickle_pure_python   | 423 us                                                                                                            | 679 us: 1.60x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 25.6 ms                                                                                                           | 31.2 ms: 1.22x slower                                                                                                   |
| python_startup_no_site | 14.4 ms                                                                                                           | 19.3 ms: 1.34x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 46.7 ms                                                                                                           | 61.0 ms: 1.31x slower                                                                                                   |
| genshi_xml      | 66.6 ms                                                                                                           | 88.9 ms: 1.33x slower                                                                                                   |
| genshi_text     | 27.6 ms                                                                                                           | 39.9 ms: 1.45x slower                                                                                                   |
| mako            | 16.5 ms                                                                                                           | 25.3 ms: 1.53x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.40x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json | results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot               | 4.60 ms                                                                                                           | 4.09 ms: 1.13x faster                                                                                                   |
| gc_traversal               | 7.52 ms                                                                                                           | 6.93 ms: 1.09x faster                                                                                                   |
| xml_etree_iterparse        | 146 ms                                                                                                            | 137 ms: 1.06x faster                                                                                                    |
| regex_dna                  | 277 ms                                                                                                            | 290 ms: 1.05x slower                                                                                                    |
| json_loads                 | 34.4 us                                                                                                           | 36.0 us: 1.05x slower                                                                                                   |
| k_core                     | 4.11 sec                                                                                                          | 4.32 sec: 1.05x slower                                                                                                  |
| xml_etree_parse            | 193 ms                                                                                                            | 205 ms: 1.06x slower                                                                                                    |
| json                       | 6.36 ms                                                                                                           | 6.95 ms: 1.09x slower                                                                                                   |
| shortest_path              | 914 ms                                                                                                            | 1.01 sec: 1.10x slower                                                                                                  |
| json_dumps                 | 15.7 ms                                                                                                           | 17.5 ms: 1.12x slower                                                                                                   |
| create_gc_cycles           | 3.31 ms                                                                                                           | 3.72 ms: 1.12x slower                                                                                                   |
| xml_etree_generate         | 121 ms                                                                                                            | 137 ms: 1.13x slower                                                                                                    |
| spectral_norm              | 135 ms                                                                                                            | 157 ms: 1.17x slower                                                                                                    |
| sqlglot_optimize           | 72.8 ms                                                                                                           | 85.0 ms: 1.17x slower                                                                                                   |
| async_tree_io_tg           | 869 ms                                                                                                            | 1.01 sec: 1.17x slower                                                                                                  |
| connected_components       | 797 ms                                                                                                            | 933 ms: 1.17x slower                                                                                                    |
| sphinx                     | 1.41 sec                                                                                                          | 1.65 sec: 1.17x slower                                                                                                  |
| async_tree_none_tg         | 378 ms                                                                                                            | 444 ms: 1.17x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 703 ms                                                                                                            | 828 ms: 1.18x slower                                                                                                    |
| pathlib                    | 26.3 ms                                                                                                           | 31.1 ms: 1.18x slower                                                                                                   |
| mdp                        | 3.76 sec                                                                                                          | 4.46 sec: 1.19x slower                                                                                                  |
| dulwich_log                | 94.6 ms                                                                                                           | 113 ms: 1.19x slower                                                                                                    |
| coroutines                 | 29.5 ms                                                                                                           | 35.3 ms: 1.19x slower                                                                                                   |
| async_tree_io              | 877 ms                                                                                                            | 1.05 sec: 1.20x slower                                                                                                  |
| docutils                   | 3.63 sec                                                                                                          | 4.37 sec: 1.20x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 673 ms                                                                                                            | 810 ms: 1.20x slower                                                                                                    |
| scimark_fft                | 440 ms                                                                                                            | 536 ms: 1.22x slower                                                                                                    |
| python_startup             | 25.6 ms                                                                                                           | 31.2 ms: 1.22x slower                                                                                                   |
| async_generators           | 534 ms                                                                                                            | 651 ms: 1.22x slower                                                                                                    |
| coverage                   | 109 ms                                                                                                            | 134 ms: 1.22x slower                                                                                                    |
| meteor_contest             | 145 ms                                                                                                            | 178 ms: 1.23x slower                                                                                                    |
| tomli_loads                | 2.68 sec                                                                                                          | 3.31 sec: 1.23x slower                                                                                                  |
| deepcopy                   | 324 us                                                                                                            | 401 us: 1.24x slower                                                                                                    |
| async_tree_memoization     | 516 ms                                                                                                            | 641 ms: 1.24x slower                                                                                                    |
| async_tree_memoization_tg  | 460 ms                                                                                                            | 572 ms: 1.24x slower                                                                                                    |
| scimark_sparse_mat_mult    | 5.91 ms                                                                                                           | 7.35 ms: 1.24x slower                                                                                                   |
| sqlglot_normalize          | 140 ms                                                                                                            | 175 ms: 1.25x slower                                                                                                    |
| regex_compile              | 171 ms                                                                                                            | 214 ms: 1.25x slower                                                                                                    |
| many_optionals             | 1.10 ms                                                                                                           | 1.38 ms: 1.25x slower                                                                                                   |
| telco                      | 10.2 ms                                                                                                           | 12.8 ms: 1.26x slower                                                                                                   |
| nqueens                    | 102 ms                                                                                                            | 129 ms: 1.27x slower                                                                                                    |
| pycparser                  | 1.52 sec                                                                                                          | 1.93 sec: 1.27x slower                                                                                                  |
| typing_runtime_protocols   | 218 us                                                                                                            | 279 us: 1.28x slower                                                                                                    |
| bpe_tokeniser              | 5.85 sec                                                                                                          | 7.55 sec: 1.29x slower                                                                                                  |
| xml_etree_process          | 78.9 ms                                                                                                           | 103 ms: 1.30x slower                                                                                                    |
| async_tree_none            | 401 ms                                                                                                            | 521 ms: 1.30x slower                                                                                                    |
| generators                 | 41.7 ms                                                                                                           | 54.3 ms: 1.30x slower                                                                                                   |
| sympy_integrate            | 29.4 ms                                                                                                           | 38.3 ms: 1.30x slower                                                                                                   |
| fannkuch                   | 524 ms                                                                                                            | 683 ms: 1.30x slower                                                                                                    |
| django_template            | 46.7 ms                                                                                                           | 61.0 ms: 1.31x slower                                                                                                   |
| deepcopy_memo              | 39.5 us                                                                                                           | 51.8 us: 1.31x slower                                                                                                   |
| deepcopy_reduce            | 3.38 us                                                                                                           | 4.47 us: 1.33x slower                                                                                                   |
| genshi_xml                 | 66.6 ms                                                                                                           | 88.9 ms: 1.33x slower                                                                                                   |
| python_startup_no_site     | 14.4 ms                                                                                                           | 19.3 ms: 1.34x slower                                                                                                   |
| pprint_pformat             | 1.98 sec                                                                                                          | 2.65 sec: 1.34x slower                                                                                                  |
| crypto_pyaes               | 91.7 ms                                                                                                           | 124 ms: 1.35x slower                                                                                                    |
| pylint                     | 386 ms                                                                                                            | 522 ms: 1.35x slower                                                                                                    |
| subparsers                 | 30.7 ms                                                                                                           | 41.6 ms: 1.35x slower                                                                                                   |
| 2to3                       | 429 ms                                                                                                            | 583 ms: 1.36x slower                                                                                                    |
| pprint_safe_repr           | 944 ms                                                                                                            | 1.29 sec: 1.36x slower                                                                                                  |
| thrift                     | 1.05 ms                                                                                                           | 1.47 ms: 1.39x slower                                                                                                   |
| nbody                      | 124 ms                                                                                                            | 173 ms: 1.40x slower                                                                                                    |
| bench_thread_pool          | 2.84 ms                                                                                                           | 3.99 ms: 1.41x slower                                                                                                   |
| unpickle_pure_python       | 290 us                                                                                                            | 414 us: 1.42x slower                                                                                                    |
| pyflate                    | 655 ms                                                                                                            | 943 ms: 1.44x slower                                                                                                    |
| genshi_text                | 27.6 ms                                                                                                           | 39.9 ms: 1.45x slower                                                                                                   |
| html5lib                   | 83.6 ms                                                                                                           | 123 ms: 1.47x slower                                                                                                    |
| richards                   | 61.7 ms                                                                                                           | 92.4 ms: 1.50x slower                                                                                                   |
| richards_super             | 70.6 ms                                                                                                           | 106 ms: 1.50x slower                                                                                                    |
| logging_format             | 8.75 us                                                                                                           | 13.2 us: 1.50x slower                                                                                                   |
| comprehensions             | 21.6 us                                                                                                           | 32.6 us: 1.51x slower                                                                                                   |
| scimark_lu                 | 146 ms                                                                                                            | 222 ms: 1.52x slower                                                                                                    |
| mako                       | 16.5 ms                                                                                                           | 25.3 ms: 1.53x slower                                                                                                   |
| float                      | 108 ms                                                                                                            | 167 ms: 1.55x slower                                                                                                    |
| sqlalchemy_declarative     | 174 ms                                                                                                            | 272 ms: 1.57x slower                                                                                                    |
| chaos                      | 80.2 ms                                                                                                           | 129 ms: 1.60x slower                                                                                                    |
| pickle_pure_python         | 423 us                                                                                                            | 679 us: 1.60x slower                                                                                                    |
| hexiom                     | 7.96 ms                                                                                                           | 12.8 ms: 1.61x slower                                                                                                   |
| logging_simple             | 7.52 us                                                                                                           | 12.3 us: 1.63x slower                                                                                                   |
| sympy_str                  | 357 ms                                                                                                            | 586 ms: 1.64x slower                                                                                                    |
| logging_silent             | 133 ns                                                                                                            | 221 ns: 1.66x slower                                                                                                    |
| sqlalchemy_imperative      | 22.2 ms                                                                                                           | 36.9 ms: 1.67x slower                                                                                                   |
| scimark_monte_carlo        | 88.0 ms                                                                                                           | 151 ms: 1.72x slower                                                                                                    |
| sqlglot_transpile          | 2.27 ms                                                                                                           | 3.99 ms: 1.76x slower                                                                                                   |
| raytrace                   | 354 ms                                                                                                            | 635 ms: 1.79x slower                                                                                                    |
| sympy_expand               | 603 ms                                                                                                            | 1.09 sec: 1.82x slower                                                                                                  |
| scimark_sor                | 156 ms                                                                                                            | 302 ms: 1.93x slower                                                                                                    |
| sqlglot_parse              | 1.70 ms                                                                                                           | 3.30 ms: 1.94x slower                                                                                                   |
| sympy_sum                  | 196 ms                                                                                                            | 400 ms: 2.04x slower                                                                                                    |
| go                         | 154 ms                                                                                                            | 315 ms: 2.05x slower                                                                                                    |
| deltablue                  | 4.31 ms                                                                                                           | 11.4 ms: 2.65x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.32x slower                                                                                                            |

Benchmark hidden because not significant (5): pidigits, asyncio_websockets, bench_mp_pool, sqlite_synth, regex_v8

- Geometric mean (including insignificant results): 1.240x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.19x