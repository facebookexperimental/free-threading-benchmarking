# Results vs. base

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.111x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 469 ms                                                                                                            | 530 ms: 1.13x slower                                                                                                    |
| docutils       | 3.58 sec                                                                                                          | 3.98 sec: 1.11x slower                                                                                                  |
| sphinx         | 1.47 sec                                                                                                          | 1.62 sec: 1.11x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 922 ms                                                                                                            | 734 ms: 1.26x faster                                                                                                    |
| async_tree_memoization_tg | 491 ms                                                                                                            | 445 ms: 1.10x faster                                                                                                    |
| async_tree_io             | 893 ms                                                                                                            | 830 ms: 1.08x faster                                                                                                    |
| async_generators          | 519 ms                                                                                                            | 563 ms: 1.08x slower                                                                                                    |
| async_tree_none           | 357 ms                                                                                                            | 389 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 659 ms                                                                                                            | 730 ms: 1.11x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (5): async_tree_none_tg, asyncio_websockets, async_tree_memoization, coroutines, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                                                                            | 181 ms: 1.45x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.70 ms                                                                                                           | 4.38 ms: 1.07x faster                                                                                                   |
| regex_compile  | 168 ms                                                                                                            | 205 ms: 1.22x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 157 ms                                                                                                            | 143 ms: 1.10x faster                                                                                                    |
| pickle_pure_python   | 434 us                                                                                                            | 458 us: 1.05x slower                                                                                                    |
| xml_etree_parse      | 207 ms                                                                                                            | 219 ms: 1.06x slower                                                                                                    |
| unpickle_pure_python | 292 us                                                                                                            | 310 us: 1.06x slower                                                                                                    |
| json_dumps           | 15.4 ms                                                                                                           | 17.4 ms: 1.13x slower                                                                                                   |
| xml_etree_process    | 83.7 ms                                                                                                           | 96.0 ms: 1.15x slower                                                                                                   |
| json_loads           | 38.7 us                                                                                                           | 44.5 us: 1.15x slower                                                                                                   |
| xml_etree_generate   | 111 ms                                                                                                            | 130 ms: 1.17x slower                                                                                                    |
| tomli_loads          | 2.53 sec                                                                                                          | 3.04 sec: 1.20x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 29.9 ms                                                                                                           | 32.3 ms: 1.08x slower                                                                                                   |
| python_startup_no_site | 18.0 ms                                                                                                           | 23.8 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 43.4 ms                                                                                                           | 55.6 ms: 1.28x slower                                                                                                   |
| genshi_xml      | 64.3 ms                                                                                                           | 84.4 ms: 1.31x slower                                                                                                   |
| mako            | 16.6 ms                                                                                                           | 22.0 ms: 1.32x slower                                                                                                   |
| genshi_text     | 28.6 ms                                                                                                           | 41.9 ms: 1.47x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.34x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal              | 8.37 ms                                                                                                           | 3.64 ms: 2.30x faster                                                                                                   |
| create_gc_cycles          | 3.76 ms                                                                                                           | 2.62 ms: 1.43x faster                                                                                                   |
| async_tree_io_tg          | 922 ms                                                                                                            | 734 ms: 1.26x faster                                                                                                    |
| async_tree_memoization_tg | 491 ms                                                                                                            | 445 ms: 1.10x faster                                                                                                    |
| xml_etree_iterparse       | 157 ms                                                                                                            | 143 ms: 1.10x faster                                                                                                    |
| async_tree_io             | 893 ms                                                                                                            | 830 ms: 1.08x faster                                                                                                    |
| regex_effbot              | 4.70 ms                                                                                                           | 4.38 ms: 1.07x faster                                                                                                   |
| pickle_pure_python        | 434 us                                                                                                            | 458 us: 1.05x slower                                                                                                    |
| k_core                    | 4.13 sec                                                                                                          | 4.36 sec: 1.06x slower                                                                                                  |
| xml_etree_parse           | 207 ms                                                                                                            | 219 ms: 1.06x slower                                                                                                    |
| unpickle_pure_python      | 292 us                                                                                                            | 310 us: 1.06x slower                                                                                                    |
| json                      | 6.95 ms                                                                                                           | 7.39 ms: 1.06x slower                                                                                                   |
| python_startup            | 29.9 ms                                                                                                           | 32.3 ms: 1.08x slower                                                                                                   |
| pylint                    | 415 ms                                                                                                            | 449 ms: 1.08x slower                                                                                                    |
| async_generators          | 519 ms                                                                                                            | 563 ms: 1.08x slower                                                                                                    |
| async_tree_none           | 357 ms                                                                                                            | 389 ms: 1.09x slower                                                                                                    |
| sphinx                    | 1.47 sec                                                                                                          | 1.62 sec: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed   | 659 ms                                                                                                            | 730 ms: 1.11x slower                                                                                                    |
| shortest_path             | 927 ms                                                                                                            | 1.03 sec: 1.11x slower                                                                                                  |
| docutils                  | 3.58 sec                                                                                                          | 3.98 sec: 1.11x slower                                                                                                  |
| bench_thread_pool         | 3.57 ms                                                                                                           | 3.98 ms: 1.12x slower                                                                                                   |
| json_dumps                | 15.4 ms                                                                                                           | 17.4 ms: 1.13x slower                                                                                                   |
| 2to3                      | 469 ms                                                                                                            | 530 ms: 1.13x slower                                                                                                    |
| telco                     | 10.7 ms                                                                                                           | 12.1 ms: 1.13x slower                                                                                                   |
| spectral_norm             | 129 ms                                                                                                            | 146 ms: 1.13x slower                                                                                                    |
| deepcopy_reduce           | 3.53 us                                                                                                           | 4.02 us: 1.14x slower                                                                                                   |
| sqlalchemy_declarative    | 191 ms                                                                                                            | 217 ms: 1.14x slower                                                                                                    |
| many_optionals            | 1.30 ms                                                                                                           | 1.48 ms: 1.14x slower                                                                                                   |
| generators                | 41.2 ms                                                                                                           | 47.0 ms: 1.14x slower                                                                                                   |
| scimark_lu                | 156 ms                                                                                                            | 179 ms: 1.15x slower                                                                                                    |
| xml_etree_process         | 83.7 ms                                                                                                           | 96.0 ms: 1.15x slower                                                                                                   |
| json_loads                | 38.7 us                                                                                                           | 44.5 us: 1.15x slower                                                                                                   |
| richards                  | 60.1 ms                                                                                                           | 69.3 ms: 1.15x slower                                                                                                   |
| logging_format            | 9.17 us                                                                                                           | 10.6 us: 1.15x slower                                                                                                   |
| sympy_str                 | 359 ms                                                                                                            | 415 ms: 1.16x slower                                                                                                    |
| sympy_expand              | 605 ms                                                                                                            | 702 ms: 1.16x slower                                                                                                    |
| mdp                       | 3.57 sec                                                                                                          | 4.16 sec: 1.16x slower                                                                                                  |
| pathlib                   | 27.6 ms                                                                                                           | 32.2 ms: 1.16x slower                                                                                                   |
| sqlglot_v2_optimize       | 72.2 ms                                                                                                           | 84.0 ms: 1.16x slower                                                                                                   |
| sqlglot_v2_normalize      | 147 ms                                                                                                            | 172 ms: 1.17x slower                                                                                                    |
| pprint_pformat            | 1.90 sec                                                                                                          | 2.22 sec: 1.17x slower                                                                                                  |
| xml_etree_generate        | 111 ms                                                                                                            | 130 ms: 1.17x slower                                                                                                    |
| fannkuch                  | 543 ms                                                                                                            | 640 ms: 1.18x slower                                                                                                    |
| pprint_safe_repr          | 922 ms                                                                                                            | 1.09 sec: 1.18x slower                                                                                                  |
| nqueens                   | 108 ms                                                                                                            | 128 ms: 1.19x slower                                                                                                    |
| connected_components      | 799 ms                                                                                                            | 949 ms: 1.19x slower                                                                                                    |
| pyflate                   | 623 ms                                                                                                            | 741 ms: 1.19x slower                                                                                                    |
| scimark_fft               | 449 ms                                                                                                            | 537 ms: 1.19x slower                                                                                                    |
| richards_super            | 70.2 ms                                                                                                           | 84.1 ms: 1.20x slower                                                                                                   |
| thrift                    | 1.03 ms                                                                                                           | 1.23 ms: 1.20x slower                                                                                                   |
| tomli_loads               | 2.53 sec                                                                                                          | 3.04 sec: 1.20x slower                                                                                                  |
| sympy_sum                 | 204 ms                                                                                                            | 247 ms: 1.21x slower                                                                                                    |
| regex_compile             | 168 ms                                                                                                            | 205 ms: 1.22x slower                                                                                                    |
| chaos                     | 77.3 ms                                                                                                           | 94.2 ms: 1.22x slower                                                                                                   |
| raytrace                  | 351 ms                                                                                                            | 428 ms: 1.22x slower                                                                                                    |
| go                        | 155 ms                                                                                                            | 189 ms: 1.22x slower                                                                                                    |
| subparsers                | 29.4 ms                                                                                                           | 35.9 ms: 1.22x slower                                                                                                   |
| bpe_tokeniser             | 6.06 sec                                                                                                          | 7.42 sec: 1.23x slower                                                                                                  |
| sympy_integrate           | 27.5 ms                                                                                                           | 33.8 ms: 1.23x slower                                                                                                   |
| comprehensions            | 21.0 us                                                                                                           | 25.9 us: 1.24x slower                                                                                                   |
| hexiom                    | 8.16 ms                                                                                                           | 10.1 ms: 1.24x slower                                                                                                   |
| logging_simple            | 8.26 us                                                                                                           | 10.3 us: 1.24x slower                                                                                                   |
| crypto_pyaes              | 100 ms                                                                                                            | 124 ms: 1.24x slower                                                                                                    |
| scimark_sor               | 151 ms                                                                                                            | 190 ms: 1.26x slower                                                                                                    |
| coverage                  | 127 ms                                                                                                            | 160 ms: 1.26x slower                                                                                                    |
| meteor_contest            | 143 ms                                                                                                            | 181 ms: 1.27x slower                                                                                                    |
| typing_runtime_protocols  | 214 us                                                                                                            | 273 us: 1.28x slower                                                                                                    |
| logging_silent            | 122 ns                                                                                                            | 157 ns: 1.28x slower                                                                                                    |
| django_template           | 43.4 ms                                                                                                           | 55.6 ms: 1.28x slower                                                                                                   |
| deepcopy                  | 330 us                                                                                                            | 427 us: 1.29x slower                                                                                                    |
| deltablue                 | 4.10 ms                                                                                                           | 5.33 ms: 1.30x slower                                                                                                   |
| scimark_monte_carlo       | 90.3 ms                                                                                                           | 118 ms: 1.30x slower                                                                                                    |
| genshi_xml                | 64.3 ms                                                                                                           | 84.4 ms: 1.31x slower                                                                                                   |
| python_startup_no_site    | 18.0 ms                                                                                                           | 23.8 ms: 1.32x slower                                                                                                   |
| mako                      | 16.6 ms                                                                                                           | 22.0 ms: 1.32x slower                                                                                                   |
| sqlglot_v2_parse          | 1.64 ms                                                                                                           | 2.21 ms: 1.35x slower                                                                                                   |
| sqlglot_v2_transpile      | 2.03 ms                                                                                                           | 2.75 ms: 1.36x slower                                                                                                   |
| deepcopy_memo             | 37.8 us                                                                                                           | 52.5 us: 1.39x slower                                                                                                   |
| sqlalchemy_imperative     | 21.8 ms                                                                                                           | 30.4 ms: 1.39x slower                                                                                                   |
| scimark_sparse_mat_mult   | 6.01 ms                                                                                                           | 8.44 ms: 1.40x slower                                                                                                   |
| nbody                     | 126 ms                                                                                                            | 181 ms: 1.45x slower                                                                                                    |
| genshi_text               | 28.6 ms                                                                                                           | 41.9 ms: 1.47x slower                                                                                                   |
| Geometric mean            | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (13): regex_v8, async_tree_none_tg, pycparser, float, asyncio_websockets, bench_mp_pool, sqlite_synth, async_tree_memoization, coroutines, async_tree_cpu_io_mixed_tg, regex_dna, pidigits, dulwich_log
Ignored benchmarks (1) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: html5lib

- Geometric mean (including insignificant results): 1.111x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x