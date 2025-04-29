# Results vs. base

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 358 ms                                                                                                            | 409 ms: 1.14x slower                                                                                                    |
| docutils       | 3.57 sec                                                                                                          | 3.86 sec: 1.08x slower                                                                                                  |
| html5lib       | 76.3 ms                                                                                                           | 83.5 ms: 1.09x slower                                                                                                   |
| sphinx         | 1.35 sec                                                                                                          | 1.54 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 829 ms                                                                                                            | 683 ms: 1.21x faster                                                                                                    |
| async_tree_none_tg         | 341 ms                                                                                                            | 295 ms: 1.15x faster                                                                                                    |
| async_tree_io              | 820 ms                                                                                                            | 728 ms: 1.13x faster                                                                                                    |
| async_tree_memoization_tg  | 443 ms                                                                                                            | 396 ms: 1.12x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                                                                            | 582 ms: 1.10x faster                                                                                                    |
| async_tree_none            | 359 ms                                                                                                            | 345 ms: 1.04x faster                                                                                                    |
| asyncio_websockets         | 660 ms                                                                                                            | 682 ms: 1.03x slower                                                                                                    |
| coroutines                 | 29.2 ms                                                                                                           | 30.3 ms: 1.04x slower                                                                                                   |
| async_tree_memoization     | 424 ms                                                                                                            | 442 ms: 1.04x slower                                                                                                    |
| async_generators           | 498 ms                                                                                                            | 534 ms: 1.07x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x faster                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 93.7 ms                                                                                                           | 91.7 ms: 1.02x faster                                                                                                   |
| pidigits       | 225 ms                                                                                                            | 237 ms: 1.06x slower                                                                                                    |
| nbody          | 118 ms                                                                                                            | 147 ms: 1.24x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 26.9 ms                                                                                                           | 26.6 ms: 1.01x faster                                                                                                   |
| regex_dna      | 253 ms                                                                                                            | 255 ms: 1.01x slower                                                                                                    |
| regex_compile  | 155 ms                                                                                                            | 181 ms: 1.17x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 144 ms                                                                                                            | 123 ms: 1.17x faster                                                                                                    |
| xml_etree_parse      | 191 ms                                                                                                            | 183 ms: 1.04x faster                                                                                                    |
| unpickle_pure_python | 274 us                                                                                                            | 295 us: 1.08x slower                                                                                                    |
| json_loads           | 38.0 us                                                                                                           | 41.4 us: 1.09x slower                                                                                                   |
| pickle_pure_python   | 391 us                                                                                                            | 437 us: 1.12x slower                                                                                                    |
| tomli_loads          | 2.45 sec                                                                                                          | 2.76 sec: 1.12x slower                                                                                                  |
| xml_etree_generate   | 116 ms                                                                                                            | 130 ms: 1.13x slower                                                                                                    |
| xml_etree_process    | 79.6 ms                                                                                                           | 91.4 ms: 1.15x slower                                                                                                   |
| json_dumps           | 14.5 ms                                                                                                           | 17.1 ms: 1.18x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 19.2 ms                                                                                                           | 24.1 ms: 1.26x slower                                                                                                   |
| python_startup_no_site | 11.6 ms                                                                                                           | 14.9 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 44.6 ms                                                                                                           | 49.0 ms: 1.10x slower                                                                                                   |
| genshi_xml      | 61.9 ms                                                                                                           | 73.4 ms: 1.18x slower                                                                                                   |
| mako            | 16.8 ms                                                                                                           | 21.0 ms: 1.25x slower                                                                                                   |
| genshi_text     | 26.3 ms                                                                                                           | 33.7 ms: 1.28x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.20x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.85 ms                                                                                                           | 3.36 ms: 2.34x faster                                                                                                   |
| create_gc_cycles           | 3.53 ms                                                                                                           | 2.41 ms: 1.47x faster                                                                                                   |
| async_tree_io_tg           | 829 ms                                                                                                            | 683 ms: 1.21x faster                                                                                                    |
| xml_etree_iterparse        | 144 ms                                                                                                            | 123 ms: 1.17x faster                                                                                                    |
| async_tree_none_tg         | 341 ms                                                                                                            | 295 ms: 1.15x faster                                                                                                    |
| sqlite_synth               | 3.27 us                                                                                                           | 2.90 us: 1.13x faster                                                                                                   |
| async_tree_io              | 820 ms                                                                                                            | 728 ms: 1.13x faster                                                                                                    |
| async_tree_memoization_tg  | 443 ms                                                                                                            | 396 ms: 1.12x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                                                                            | 582 ms: 1.10x faster                                                                                                    |
| pycparser                  | 1.50 sec                                                                                                          | 1.44 sec: 1.04x faster                                                                                                  |
| xml_etree_parse            | 191 ms                                                                                                            | 183 ms: 1.04x faster                                                                                                    |
| async_tree_none            | 359 ms                                                                                                            | 345 ms: 1.04x faster                                                                                                    |
| float                      | 93.7 ms                                                                                                           | 91.7 ms: 1.02x faster                                                                                                   |
| regex_v8                   | 26.9 ms                                                                                                           | 26.6 ms: 1.01x faster                                                                                                   |
| regex_dna                  | 253 ms                                                                                                            | 255 ms: 1.01x slower                                                                                                    |
| pathlib                    | 25.1 ms                                                                                                           | 25.9 ms: 1.03x slower                                                                                                   |
| asyncio_websockets         | 660 ms                                                                                                            | 682 ms: 1.03x slower                                                                                                    |
| json                       | 6.81 ms                                                                                                           | 7.06 ms: 1.04x slower                                                                                                   |
| coroutines                 | 29.2 ms                                                                                                           | 30.3 ms: 1.04x slower                                                                                                   |
| async_tree_memoization     | 424 ms                                                                                                            | 442 ms: 1.04x slower                                                                                                    |
| pidigits                   | 225 ms                                                                                                            | 237 ms: 1.06x slower                                                                                                    |
| k_core                     | 3.78 sec                                                                                                          | 4.00 sec: 1.06x slower                                                                                                  |
| bench_thread_pool          | 2.55 ms                                                                                                           | 2.71 ms: 1.07x slower                                                                                                   |
| deltablue                  | 4.35 ms                                                                                                           | 4.66 ms: 1.07x slower                                                                                                   |
| async_generators           | 498 ms                                                                                                            | 534 ms: 1.07x slower                                                                                                    |
| dulwich_log                | 74.1 ms                                                                                                           | 79.7 ms: 1.08x slower                                                                                                   |
| unpickle_pure_python       | 274 us                                                                                                            | 295 us: 1.08x slower                                                                                                    |
| docutils                   | 3.57 sec                                                                                                          | 3.86 sec: 1.08x slower                                                                                                  |
| scimark_sor                | 144 ms                                                                                                            | 156 ms: 1.09x slower                                                                                                    |
| generators                 | 39.8 ms                                                                                                           | 43.4 ms: 1.09x slower                                                                                                   |
| json_loads                 | 38.0 us                                                                                                           | 41.4 us: 1.09x slower                                                                                                   |
| pylint                     | 386 ms                                                                                                            | 421 ms: 1.09x slower                                                                                                    |
| html5lib                   | 76.3 ms                                                                                                           | 83.5 ms: 1.09x slower                                                                                                   |
| scimark_fft                | 424 ms                                                                                                            | 465 ms: 1.10x slower                                                                                                    |
| django_template            | 44.6 ms                                                                                                           | 49.0 ms: 1.10x slower                                                                                                   |
| telco                      | 9.25 ms                                                                                                           | 10.2 ms: 1.11x slower                                                                                                   |
| connected_components       | 756 ms                                                                                                            | 842 ms: 1.11x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.03 ms                                                                                                           | 6.73 ms: 1.12x slower                                                                                                   |
| sqlglot_v2_normalize       | 131 ms                                                                                                            | 146 ms: 1.12x slower                                                                                                    |
| pickle_pure_python         | 391 us                                                                                                            | 437 us: 1.12x slower                                                                                                    |
| logging_silent             | 126 ns                                                                                                            | 141 ns: 1.12x slower                                                                                                    |
| tomli_loads                | 2.45 sec                                                                                                          | 2.76 sec: 1.12x slower                                                                                                  |
| xml_etree_generate         | 116 ms                                                                                                            | 130 ms: 1.13x slower                                                                                                    |
| pyflate                    | 573 ms                                                                                                            | 651 ms: 1.13x slower                                                                                                    |
| shortest_path              | 824 ms                                                                                                            | 938 ms: 1.14x slower                                                                                                    |
| spectral_norm              | 125 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| deepcopy_reduce            | 3.41 us                                                                                                           | 3.89 us: 1.14x slower                                                                                                   |
| 2to3                       | 358 ms                                                                                                            | 409 ms: 1.14x slower                                                                                                    |
| deepcopy                   | 324 us                                                                                                            | 371 us: 1.15x slower                                                                                                    |
| nqueens                    | 97.7 ms                                                                                                           | 112 ms: 1.15x slower                                                                                                    |
| sphinx                     | 1.35 sec                                                                                                          | 1.54 sec: 1.15x slower                                                                                                  |
| scimark_lu                 | 147 ms                                                                                                            | 168 ms: 1.15x slower                                                                                                    |
| chaos                      | 70.7 ms                                                                                                           | 81.1 ms: 1.15x slower                                                                                                   |
| xml_etree_process          | 79.6 ms                                                                                                           | 91.4 ms: 1.15x slower                                                                                                   |
| logging_simple             | 7.64 us                                                                                                           | 8.82 us: 1.16x slower                                                                                                   |
| raytrace                   | 330 ms                                                                                                            | 382 ms: 1.16x slower                                                                                                    |
| sqlglot_v2_optimize        | 66.3 ms                                                                                                           | 76.8 ms: 1.16x slower                                                                                                   |
| many_optionals             | 1.14 ms                                                                                                           | 1.32 ms: 1.16x slower                                                                                                   |
| go                         | 140 ms                                                                                                            | 163 ms: 1.16x slower                                                                                                    |
| pprint_pformat             | 1.81 sec                                                                                                          | 2.10 sec: 1.16x slower                                                                                                  |
| pprint_safe_repr           | 886 ms                                                                                                            | 1.03 sec: 1.16x slower                                                                                                  |
| subparsers                 | 28.0 ms                                                                                                           | 32.7 ms: 1.17x slower                                                                                                   |
| regex_compile              | 155 ms                                                                                                            | 181 ms: 1.17x slower                                                                                                    |
| thrift                     | 949 us                                                                                                            | 1.11 ms: 1.17x slower                                                                                                   |
| sympy_expand               | 558 ms                                                                                                            | 652 ms: 1.17x slower                                                                                                    |
| hexiom                     | 7.49 ms                                                                                                           | 8.78 ms: 1.17x slower                                                                                                   |
| logging_format             | 8.49 us                                                                                                           | 9.98 us: 1.17x slower                                                                                                   |
| json_dumps                 | 14.5 ms                                                                                                           | 17.1 ms: 1.18x slower                                                                                                   |
| genshi_xml                 | 61.9 ms                                                                                                           | 73.4 ms: 1.18x slower                                                                                                   |
| sympy_sum                  | 187 ms                                                                                                            | 222 ms: 1.19x slower                                                                                                    |
| comprehensions             | 21.1 us                                                                                                           | 25.4 us: 1.20x slower                                                                                                   |
| sympy_integrate            | 24.7 ms                                                                                                           | 29.8 ms: 1.20x slower                                                                                                   |
| fannkuch                   | 495 ms                                                                                                            | 596 ms: 1.20x slower                                                                                                    |
| sympy_str                  | 330 ms                                                                                                            | 400 ms: 1.21x slower                                                                                                    |
| richards_super             | 63.0 ms                                                                                                           | 76.4 ms: 1.21x slower                                                                                                   |
| crypto_pyaes               | 89.8 ms                                                                                                           | 110 ms: 1.22x slower                                                                                                    |
| richards                   | 54.6 ms                                                                                                           | 66.7 ms: 1.22x slower                                                                                                   |
| typing_runtime_protocols   | 200 us                                                                                                            | 245 us: 1.23x slower                                                                                                    |
| mdp                        | 1.84 sec                                                                                                          | 2.27 sec: 1.23x slower                                                                                                  |
| sqlglot_v2_parse           | 1.58 ms                                                                                                           | 1.95 ms: 1.23x slower                                                                                                   |
| scimark_monte_carlo        | 80.3 ms                                                                                                           | 99.2 ms: 1.24x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.97 ms                                                                                                           | 2.43 ms: 1.24x slower                                                                                                   |
| nbody                      | 118 ms                                                                                                            | 147 ms: 1.24x slower                                                                                                    |
| deepcopy_memo              | 36.9 us                                                                                                           | 45.8 us: 1.24x slower                                                                                                   |
| mako                       | 16.8 ms                                                                                                           | 21.0 ms: 1.25x slower                                                                                                   |
| python_startup             | 19.2 ms                                                                                                           | 24.1 ms: 1.26x slower                                                                                                   |
| meteor_contest             | 127 ms                                                                                                            | 160 ms: 1.26x slower                                                                                                    |
| python_startup_no_site     | 11.6 ms                                                                                                           | 14.9 ms: 1.28x slower                                                                                                   |
| genshi_text                | 26.3 ms                                                                                                           | 33.7 ms: 1.28x slower                                                                                                   |
| bpe_tokeniser              | 5.55 sec                                                                                                          | 7.15 sec: 1.29x slower                                                                                                  |
| coverage                   | 107 ms                                                                                                            | 146 ms: 1.37x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, bench_mp_pool, regex_effbot

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x