# Results vs. base

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.128x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 476 ms                                                                                                            | 580 ms: 1.22x slower                                                                                                    |
| docutils       | 3.71 sec                                                                                                          | 4.47 sec: 1.20x slower                                                                                                  |
| html5lib       | 89.6 ms                                                                                                           | 108 ms: 1.20x slower                                                                                                    |
| sphinx         | 1.46 sec                                                                                                          | 1.64 sec: 1.12x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 909 ms                                                                                                            | 753 ms: 1.21x faster                                                                                                    |
| async_tree_none_tg         | 364 ms                                                                                                            | 335 ms: 1.09x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 649 ms                                                                                                            | 683 ms: 1.05x slower                                                                                                    |
| async_generators           | 539 ms                                                                                                            | 573 ms: 1.06x slower                                                                                                    |
| coroutines                 | 31.1 ms                                                                                                           | 33.7 ms: 1.08x slower                                                                                                   |
| asyncio_websockets         | 716 ms                                                                                                            | 776 ms: 1.08x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 660 ms                                                                                                            | 749 ms: 1.13x slower                                                                                                    |
| async_tree_memoization     | 490 ms                                                                                                            | 586 ms: 1.20x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 258 ms                                                                                                            | 243 ms: 1.06x faster                                                                                                    |
| nbody          | 129 ms                                                                                                            | 192 ms: 1.49x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                                                            | 309 ms: 1.09x slower                                                                                                    |
| regex_compile  | 180 ms                                                                                                            | 224 ms: 1.24x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 156 ms                                                                                                            | 140 ms: 1.11x faster                                                                                                    |
| xml_etree_parse      | 215 ms                                                                                                            | 231 ms: 1.08x slower                                                                                                    |
| xml_etree_generate   | 124 ms                                                                                                            | 135 ms: 1.09x slower                                                                                                    |
| pickle_pure_python   | 438 us                                                                                                            | 492 us: 1.12x slower                                                                                                    |
| unpickle_pure_python | 316 us                                                                                                            | 361 us: 1.14x slower                                                                                                    |
| tomli_loads          | 2.61 sec                                                                                                          | 3.04 sec: 1.16x slower                                                                                                  |
| json_loads           | 39.6 us                                                                                                           | 46.2 us: 1.16x slower                                                                                                   |
| xml_etree_process    | 88.7 ms                                                                                                           | 107 ms: 1.20x slower                                                                                                    |
| json_dumps           | 15.6 ms                                                                                                           | 19.4 ms: 1.24x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 30.3 ms                                                                                                           | 35.1 ms: 1.16x slower                                                                                                   |
| python_startup_no_site | 18.4 ms                                                                                                           | 22.4 ms: 1.22x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 49.7 ms                                                                                                           | 60.3 ms: 1.21x slower                                                                                                   |
| genshi_xml      | 68.1 ms                                                                                                           | 89.2 ms: 1.31x slower                                                                                                   |
| genshi_text     | 28.5 ms                                                                                                           | 40.7 ms: 1.43x slower                                                                                                   |
| mako            | 16.1 ms                                                                                                           | 24.8 ms: 1.54x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.37x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 3.93 ms                                                                                                           | 3.20 ms: 1.23x faster                                                                                                   |
| async_tree_io_tg           | 909 ms                                                                                                            | 753 ms: 1.21x faster                                                                                                    |
| xml_etree_iterparse        | 156 ms                                                                                                            | 140 ms: 1.11x faster                                                                                                    |
| gc_traversal               | 9.71 ms                                                                                                           | 8.76 ms: 1.11x faster                                                                                                   |
| async_tree_none_tg         | 364 ms                                                                                                            | 335 ms: 1.09x faster                                                                                                    |
| pidigits                   | 258 ms                                                                                                            | 243 ms: 1.06x faster                                                                                                    |
| sqlite_synth               | 3.82 us                                                                                                           | 3.63 us: 1.05x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 649 ms                                                                                                            | 683 ms: 1.05x slower                                                                                                    |
| k_core                     | 4.22 sec                                                                                                          | 4.46 sec: 1.06x slower                                                                                                  |
| async_generators           | 539 ms                                                                                                            | 573 ms: 1.06x slower                                                                                                    |
| spectral_norm              | 143 ms                                                                                                            | 152 ms: 1.06x slower                                                                                                    |
| xml_etree_parse            | 215 ms                                                                                                            | 231 ms: 1.08x slower                                                                                                    |
| generators                 | 42.8 ms                                                                                                           | 46.4 ms: 1.08x slower                                                                                                   |
| coroutines                 | 31.1 ms                                                                                                           | 33.7 ms: 1.08x slower                                                                                                   |
| asyncio_websockets         | 716 ms                                                                                                            | 776 ms: 1.08x slower                                                                                                    |
| xml_etree_generate         | 124 ms                                                                                                            | 135 ms: 1.09x slower                                                                                                    |
| pprint_safe_repr           | 1.02 sec                                                                                                          | 1.11 sec: 1.09x slower                                                                                                  |
| regex_dna                  | 284 ms                                                                                                            | 309 ms: 1.09x slower                                                                                                    |
| telco                      | 11.8 ms                                                                                                           | 13.0 ms: 1.10x slower                                                                                                   |
| sphinx                     | 1.46 sec                                                                                                          | 1.64 sec: 1.12x slower                                                                                                  |
| pickle_pure_python         | 438 us                                                                                                            | 492 us: 1.12x slower                                                                                                    |
| shortest_path              | 922 ms                                                                                                            | 1.04 sec: 1.13x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 660 ms                                                                                                            | 749 ms: 1.13x slower                                                                                                    |
| chaos                      | 87.3 ms                                                                                                           | 99.1 ms: 1.13x slower                                                                                                   |
| pyflate                    | 678 ms                                                                                                            | 772 ms: 1.14x slower                                                                                                    |
| subparsers                 | 33.9 ms                                                                                                           | 38.6 ms: 1.14x slower                                                                                                   |
| unpickle_pure_python       | 316 us                                                                                                            | 361 us: 1.14x slower                                                                                                    |
| sympy_expand               | 602 ms                                                                                                            | 689 ms: 1.14x slower                                                                                                    |
| pprint_pformat             | 2.06 sec                                                                                                          | 2.36 sec: 1.15x slower                                                                                                  |
| typing_runtime_protocols   | 263 us                                                                                                            | 302 us: 1.15x slower                                                                                                    |
| logging_silent             | 139 ns                                                                                                            | 161 ns: 1.16x slower                                                                                                    |
| python_startup             | 30.3 ms                                                                                                           | 35.1 ms: 1.16x slower                                                                                                   |
| richards                   | 60.6 ms                                                                                                           | 70.4 ms: 1.16x slower                                                                                                   |
| tomli_loads                | 2.61 sec                                                                                                          | 3.04 sec: 1.16x slower                                                                                                  |
| json_loads                 | 39.6 us                                                                                                           | 46.2 us: 1.16x slower                                                                                                   |
| connected_components       | 853 ms                                                                                                            | 995 ms: 1.17x slower                                                                                                    |
| mdp                        | 3.84 sec                                                                                                          | 4.48 sec: 1.17x slower                                                                                                  |
| pylint                     | 413 ms                                                                                                            | 486 ms: 1.17x slower                                                                                                    |
| sympy_integrate            | 28.3 ms                                                                                                           | 33.6 ms: 1.18x slower                                                                                                   |
| logging_format             | 11.2 us                                                                                                           | 13.2 us: 1.19x slower                                                                                                   |
| scimark_sor                | 167 ms                                                                                                            | 199 ms: 1.19x slower                                                                                                    |
| many_optionals             | 1.24 ms                                                                                                           | 1.47 ms: 1.19x slower                                                                                                   |
| comprehensions             | 22.1 us                                                                                                           | 26.4 us: 1.19x slower                                                                                                   |
| async_tree_memoization     | 490 ms                                                                                                            | 586 ms: 1.20x slower                                                                                                    |
| xml_etree_process          | 88.7 ms                                                                                                           | 107 ms: 1.20x slower                                                                                                    |
| html5lib                   | 89.6 ms                                                                                                           | 108 ms: 1.20x slower                                                                                                    |
| docutils                   | 3.71 sec                                                                                                          | 4.47 sec: 1.20x slower                                                                                                  |
| django_template            | 49.7 ms                                                                                                           | 60.3 ms: 1.21x slower                                                                                                   |
| go                         | 151 ms                                                                                                            | 183 ms: 1.22x slower                                                                                                    |
| 2to3                       | 476 ms                                                                                                            | 580 ms: 1.22x slower                                                                                                    |
| python_startup_no_site     | 18.4 ms                                                                                                           | 22.4 ms: 1.22x slower                                                                                                   |
| scimark_lu                 | 157 ms                                                                                                            | 195 ms: 1.24x slower                                                                                                    |
| regex_compile              | 180 ms                                                                                                            | 224 ms: 1.24x slower                                                                                                    |
| json_dumps                 | 15.6 ms                                                                                                           | 19.4 ms: 1.24x slower                                                                                                   |
| nqueens                    | 111 ms                                                                                                            | 139 ms: 1.25x slower                                                                                                    |
| coverage                   | 120 ms                                                                                                            | 150 ms: 1.25x slower                                                                                                    |
| deepcopy                   | 360 us                                                                                                            | 449 us: 1.25x slower                                                                                                    |
| logging_simple             | 9.03 us                                                                                                           | 11.3 us: 1.25x slower                                                                                                   |
| scimark_monte_carlo        | 96.3 ms                                                                                                           | 121 ms: 1.26x slower                                                                                                    |
| sympy_sum                  | 197 ms                                                                                                            | 249 ms: 1.27x slower                                                                                                    |
| scimark_fft                | 453 ms                                                                                                            | 574 ms: 1.27x slower                                                                                                    |
| thrift                     | 1.17 ms                                                                                                           | 1.49 ms: 1.27x slower                                                                                                   |
| richards_super             | 66.8 ms                                                                                                           | 85.9 ms: 1.29x slower                                                                                                   |
| crypto_pyaes               | 99.8 ms                                                                                                           | 129 ms: 1.29x slower                                                                                                    |
| hexiom                     | 8.85 ms                                                                                                           | 11.5 ms: 1.30x slower                                                                                                   |
| meteor_contest             | 144 ms                                                                                                            | 188 ms: 1.30x slower                                                                                                    |
| genshi_xml                 | 68.1 ms                                                                                                           | 89.2 ms: 1.31x slower                                                                                                   |
| scimark_sparse_mat_mult    | 6.61 ms                                                                                                           | 8.68 ms: 1.31x slower                                                                                                   |
| raytrace                   | 383 ms                                                                                                            | 503 ms: 1.31x slower                                                                                                    |
| fannkuch                   | 514 ms                                                                                                            | 679 ms: 1.32x slower                                                                                                    |
| deepcopy_memo              | 40.1 us                                                                                                           | 53.0 us: 1.32x slower                                                                                                   |
| bpe_tokeniser              | 5.89 sec                                                                                                          | 7.86 sec: 1.33x slower                                                                                                  |
| sqlglot_parse              | 1.75 ms                                                                                                           | 2.36 ms: 1.35x slower                                                                                                   |
| deepcopy_reduce            | 3.38 us                                                                                                           | 4.65 us: 1.37x slower                                                                                                   |
| genshi_text                | 28.5 ms                                                                                                           | 40.7 ms: 1.43x slower                                                                                                   |
| sqlalchemy_imperative      | 23.7 ms                                                                                                           | 33.9 ms: 1.43x slower                                                                                                   |
| sqlalchemy_declarative     | 164 ms                                                                                                            | 239 ms: 1.45x slower                                                                                                    |
| nbody                      | 129 ms                                                                                                            | 192 ms: 1.49x slower                                                                                                    |
| mako                       | 16.1 ms                                                                                                           | 24.8 ms: 1.54x slower                                                                                                   |
| bench_thread_pool          | 3.81 ms                                                                                                           | 5.88 ms: 1.54x slower                                                                                                   |
| sqlglot_transpile          | 2.20 ms                                                                                                           | 3.59 ms: 1.63x slower                                                                                                   |
| deltablue                  | 4.28 ms                                                                                                           | 7.11 ms: 1.66x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (14): json, regex_effbot, float, async_tree_memoization_tg, async_tree_io, dulwich_log, bench_mp_pool, pycparser, pathlib, sqlglot_optimize, async_tree_none, sqlglot_normalize, sympy_str, regex_v8

- Geometric mean (including insignificant results): 1.128x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x