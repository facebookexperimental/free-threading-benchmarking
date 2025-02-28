# Results vs. base

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.150x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                            | 305 ms: 1.23x slower                                                                                                    |
| docutils       | 2.53 sec                                                                                                          | 2.80 sec: 1.11x slower                                                                                                  |
| sphinx         | 967 ms                                                                                                            | 1.11 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 602 ms                                                                                                            | 551 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 251 ms                                                                                                            | 238 ms: 1.05x faster                                                                                                    |
| async_tree_io              | 604 ms                                                                                                            | 581 ms: 1.04x faster                                                                                                    |
| async_tree_none            | 257 ms                                                                                                            | 275 ms: 1.07x slower                                                                                                    |
| async_tree_memoization     | 312 ms                                                                                                            | 337 ms: 1.08x slower                                                                                                    |
| coroutines                 | 21.1 ms                                                                                                           | 23.2 ms: 1.10x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                                                            | 542 ms: 1.15x slower                                                                                                    |
| async_generators           | 322 ms                                                                                                            | 372 ms: 1.16x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 484 ms                                                                                                            | 575 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                                                            | 210 ms: 1.06x slower                                                                                                    |
| float          | 71.5 ms                                                                                                           | 76.3 ms: 1.07x slower                                                                                                   |
| nbody          | 87.3 ms                                                                                                           | 135 ms: 1.55x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                                                           | 24.4 ms: 1.03x faster                                                                                                   |
| regex_dna      | 176 ms                                                                                                            | 183 ms: 1.04x slower                                                                                                    |
| regex_compile  | 123 ms                                                                                                            | 157 ms: 1.27x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.0 ms                                                                                                           | 87.8 ms: 1.03x faster                                                                                                   |
| json_loads           | 28.0 us                                                                                                           | 29.6 us: 1.06x slower                                                                                                   |
| xml_etree_generate   | 82.8 ms                                                                                                           | 95.4 ms: 1.15x slower                                                                                                   |
| json_dumps           | 11.1 ms                                                                                                           | 13.1 ms: 1.17x slower                                                                                                   |
| unpickle_pure_python | 208 us                                                                                                            | 251 us: 1.21x slower                                                                                                    |
| pickle_pure_python   | 303 us                                                                                                            | 367 us: 1.21x slower                                                                                                    |
| xml_etree_process    | 57.3 ms                                                                                                           | 69.5 ms: 1.21x slower                                                                                                   |
| tomli_loads          | 1.88 sec                                                                                                          | 2.36 sec: 1.26x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.6 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 7.51 ms                                                                                                           | 9.64 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.4 ms                                                                                                           | 60.0 ms: 1.26x slower                                                                                                   |
| django_template | 32.9 ms                                                                                                           | 43.3 ms: 1.32x slower                                                                                                   |
| genshi_text     | 20.4 ms                                                                                                           | 27.9 ms: 1.37x slower                                                                                                   |
| mako            | 11.5 ms                                                                                                           | 15.9 ms: 1.39x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.33x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.46 ms                                                                                                           | 1.71 ms: 2.60x faster                                                                                                   |
| create_gc_cycles           | 1.83 ms                                                                                                           | 1.30 ms: 1.41x faster                                                                                                   |
| async_tree_io_tg           | 602 ms                                                                                                            | 551 ms: 1.09x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.04 us: 1.07x faster                                                                                                   |
| async_tree_none_tg         | 251 ms                                                                                                            | 238 ms: 1.05x faster                                                                                                    |
| async_tree_io              | 604 ms                                                                                                            | 581 ms: 1.04x faster                                                                                                    |
| regex_v8                   | 25.2 ms                                                                                                           | 24.4 ms: 1.03x faster                                                                                                   |
| xml_etree_iterparse        | 90.0 ms                                                                                                           | 87.8 ms: 1.03x faster                                                                                                   |
| pathlib                    | 18.8 ms                                                                                                           | 19.4 ms: 1.04x slower                                                                                                   |
| regex_dna                  | 176 ms                                                                                                            | 183 ms: 1.04x slower                                                                                                    |
| json                       | 4.92 ms                                                                                                           | 5.12 ms: 1.04x slower                                                                                                   |
| json_loads                 | 28.0 us                                                                                                           | 29.6 us: 1.06x slower                                                                                                   |
| python_startup             | 14.7 ms                                                                                                           | 15.6 ms: 1.06x slower                                                                                                   |
| pidigits                   | 198 ms                                                                                                            | 210 ms: 1.06x slower                                                                                                    |
| float                      | 71.5 ms                                                                                                           | 76.3 ms: 1.07x slower                                                                                                   |
| async_tree_none            | 257 ms                                                                                                            | 275 ms: 1.07x slower                                                                                                    |
| pycparser                  | 1.11 sec                                                                                                          | 1.19 sec: 1.07x slower                                                                                                  |
| bench_mp_pool              | 88.1 ms                                                                                                           | 95.0 ms: 1.08x slower                                                                                                   |
| async_tree_memoization     | 312 ms                                                                                                            | 337 ms: 1.08x slower                                                                                                    |
| logging_silent             | 103 ns                                                                                                            | 112 ns: 1.09x slower                                                                                                    |
| coroutines                 | 21.1 ms                                                                                                           | 23.2 ms: 1.10x slower                                                                                                   |
| dulwich_log                | 74.7 ms                                                                                                           | 82.6 ms: 1.11x slower                                                                                                   |
| docutils                   | 2.53 sec                                                                                                          | 2.80 sec: 1.11x slower                                                                                                  |
| sphinx                     | 967 ms                                                                                                            | 1.11 sec: 1.15x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                                                            | 542 ms: 1.15x slower                                                                                                    |
| pylint                     | 273 ms                                                                                                            | 315 ms: 1.15x slower                                                                                                    |
| xml_etree_generate         | 82.8 ms                                                                                                           | 95.4 ms: 1.15x slower                                                                                                   |
| k_core                     | 2.01 sec                                                                                                          | 2.32 sec: 1.15x slower                                                                                                  |
| async_generators           | 322 ms                                                                                                            | 372 ms: 1.16x slower                                                                                                    |
| bpe_tokeniser              | 4.13 sec                                                                                                          | 4.80 sec: 1.16x slower                                                                                                  |
| subparsers                 | 21.7 ms                                                                                                           | 25.2 ms: 1.17x slower                                                                                                   |
| many_optionals             | 1.00 ms                                                                                                           | 1.17 ms: 1.17x slower                                                                                                   |
| mdp                        | 2.29 sec                                                                                                          | 2.68 sec: 1.17x slower                                                                                                  |
| generators                 | 26.8 ms                                                                                                           | 31.3 ms: 1.17x slower                                                                                                   |
| json_dumps                 | 11.1 ms                                                                                                           | 13.1 ms: 1.17x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 484 ms                                                                                                            | 575 ms: 1.19x slower                                                                                                    |
| unpickle_pure_python       | 208 us                                                                                                            | 251 us: 1.21x slower                                                                                                    |
| pickle_pure_python         | 303 us                                                                                                            | 367 us: 1.21x slower                                                                                                    |
| xml_etree_process          | 57.3 ms                                                                                                           | 69.5 ms: 1.21x slower                                                                                                   |
| sqlglot_optimize           | 50.7 ms                                                                                                           | 61.6 ms: 1.21x slower                                                                                                   |
| telco                      | 7.15 ms                                                                                                           | 8.75 ms: 1.22x slower                                                                                                   |
| sqlglot_normalize          | 99.8 ms                                                                                                           | 122 ms: 1.22x slower                                                                                                    |
| coverage                   | 79.5 ms                                                                                                           | 97.2 ms: 1.22x slower                                                                                                   |
| logging_simple             | 5.91 us                                                                                                           | 7.24 us: 1.23x slower                                                                                                   |
| 2to3                       | 249 ms                                                                                                            | 305 ms: 1.23x slower                                                                                                    |
| thrift                     | 715 us                                                                                                            | 881 us: 1.23x slower                                                                                                    |
| pyflate                    | 403 ms                                                                                                            | 498 ms: 1.24x slower                                                                                                    |
| sympy_expand               | 450 ms                                                                                                            | 558 ms: 1.24x slower                                                                                                    |
| pprint_safe_repr           | 681 ms                                                                                                            | 844 ms: 1.24x slower                                                                                                    |
| sqlalchemy_declarative     | 126 ms                                                                                                            | 156 ms: 1.24x slower                                                                                                    |
| sqlglot_transpile          | 1.54 ms                                                                                                           | 1.92 ms: 1.24x slower                                                                                                   |
| sqlalchemy_imperative      | 19.0 ms                                                                                                           | 23.7 ms: 1.25x slower                                                                                                   |
| deltablue                  | 3.02 ms                                                                                                           | 3.78 ms: 1.25x slower                                                                                                   |
| sympy_sum                  | 150 ms                                                                                                            | 188 ms: 1.25x slower                                                                                                    |
| sympy_integrate            | 19.3 ms                                                                                                           | 24.2 ms: 1.25x slower                                                                                                   |
| comprehensions             | 16.0 us                                                                                                           | 20.0 us: 1.26x slower                                                                                                   |
| pprint_pformat             | 1.38 sec                                                                                                          | 1.74 sec: 1.26x slower                                                                                                  |
| tomli_loads                | 1.88 sec                                                                                                          | 2.36 sec: 1.26x slower                                                                                                  |
| deepcopy_reduce            | 2.53 us                                                                                                           | 3.17 us: 1.26x slower                                                                                                   |
| logging_format             | 6.60 us                                                                                                           | 8.32 us: 1.26x slower                                                                                                   |
| raytrace                   | 253 ms                                                                                                            | 319 ms: 1.26x slower                                                                                                    |
| genshi_xml                 | 47.4 ms                                                                                                           | 60.0 ms: 1.26x slower                                                                                                   |
| spectral_norm              | 90.6 ms                                                                                                           | 115 ms: 1.27x slower                                                                                                    |
| chaos                      | 54.5 ms                                                                                                           | 69.3 ms: 1.27x slower                                                                                                   |
| regex_compile              | 123 ms                                                                                                            | 157 ms: 1.27x slower                                                                                                    |
| deepcopy                   | 244 us                                                                                                            | 310 us: 1.27x slower                                                                                                    |
| sqlglot_parse              | 1.25 ms                                                                                                           | 1.59 ms: 1.27x slower                                                                                                   |
| sympy_str                  | 267 ms                                                                                                            | 341 ms: 1.28x slower                                                                                                    |
| go                         | 110 ms                                                                                                            | 141 ms: 1.28x slower                                                                                                    |
| shortest_path              | 427 ms                                                                                                            | 548 ms: 1.28x slower                                                                                                    |
| python_startup_no_site     | 7.51 ms                                                                                                           | 9.64 ms: 1.28x slower                                                                                                   |
| connected_components       | 386 ms                                                                                                            | 498 ms: 1.29x slower                                                                                                    |
| scimark_sor                | 112 ms                                                                                                            | 144 ms: 1.29x slower                                                                                                    |
| typing_runtime_protocols   | 153 us                                                                                                            | 199 us: 1.30x slower                                                                                                    |
| deepcopy_memo              | 29.2 us                                                                                                           | 38.1 us: 1.30x slower                                                                                                   |
| richards                   | 41.9 ms                                                                                                           | 54.7 ms: 1.30x slower                                                                                                   |
| hexiom                     | 5.70 ms                                                                                                           | 7.45 ms: 1.31x slower                                                                                                   |
| nqueens                    | 74.9 ms                                                                                                           | 98.1 ms: 1.31x slower                                                                                                   |
| meteor_contest             | 97.1 ms                                                                                                           | 128 ms: 1.32x slower                                                                                                    |
| django_template            | 32.9 ms                                                                                                           | 43.3 ms: 1.32x slower                                                                                                   |
| crypto_pyaes               | 66.2 ms                                                                                                           | 88.0 ms: 1.33x slower                                                                                                   |
| richards_super             | 47.9 ms                                                                                                           | 63.9 ms: 1.33x slower                                                                                                   |
| fannkuch                   | 363 ms                                                                                                            | 494 ms: 1.36x slower                                                                                                    |
| genshi_text                | 20.4 ms                                                                                                           | 27.9 ms: 1.37x slower                                                                                                   |
| mako                       | 11.5 ms                                                                                                           | 15.9 ms: 1.39x slower                                                                                                   |
| scimark_lu                 | 112 ms                                                                                                            | 156 ms: 1.39x slower                                                                                                    |
| scimark_fft                | 331 ms                                                                                                            | 493 ms: 1.49x slower                                                                                                    |
| scimark_monte_carlo        | 63.4 ms                                                                                                           | 95.3 ms: 1.50x slower                                                                                                   |
| nbody                      | 87.3 ms                                                                                                           | 135 ms: 1.55x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.26 ms                                                                                                           | 7.76 ms: 1.82x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.31 ms: 3.22x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (4): xml_etree_parse, asyncio_websockets, async_tree_memoization_tg, regex_effbot
Ignored benchmarks (1) of results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: html5lib

- Geometric mean (including insignificant results): 1.150x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.20x