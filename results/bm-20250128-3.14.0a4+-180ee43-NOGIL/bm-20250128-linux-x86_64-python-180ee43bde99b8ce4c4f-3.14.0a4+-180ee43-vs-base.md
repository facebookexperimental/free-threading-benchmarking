# Results vs. base

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.141x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 529 ms                                                                                                            | 620 ms: 1.17x slower                                                                                                    |
| docutils       | 3.90 sec                                                                                                          | 4.25 sec: 1.09x slower                                                                                                  |
| html5lib       | 77.2 ms                                                                                                           | 102 ms: 1.32x slower                                                                                                    |
| sphinx         | 1.50 sec                                                                                                          | 1.65 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 906 ms                                                                                                            | 838 ms: 1.08x faster                                                                                                    |
| coroutines                | 34.7 ms                                                                                                           | 32.3 ms: 1.07x faster                                                                                                   |
| async_tree_none           | 425 ms                                                                                                            | 449 ms: 1.06x slower                                                                                                    |
| async_generators          | 554 ms                                                                                                            | 610 ms: 1.10x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 727 ms                                                                                                            | 822 ms: 1.13x slower                                                                                                    |
| async_tree_memoization_tg | 455 ms                                                                                                            | 517 ms: 1.14x slower                                                                                                    |
| async_tree_none_tg        | 376 ms                                                                                                            | 429 ms: 1.14x slower                                                                                                    |
| asyncio_websockets        | 701 ms                                                                                                            | 811 ms: 1.16x slower                                                                                                    |
| async_tree_memoization    | 491 ms                                                                                                            | 632 ms: 1.29x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 243 ms                                                                                                            | 264 ms: 1.09x slower                                                                                                    |
| nbody          | 130 ms                                                                                                            | 192 ms: 1.47x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 286 ms                                                                                                            | 301 ms: 1.05x slower                                                                                                    |
| regex_effbot   | 4.20 ms                                                                                                           | 4.53 ms: 1.08x slower                                                                                                   |
| regex_compile  | 188 ms                                                                                                            | 224 ms: 1.20x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 345 us                                                                                                            | 371 us: 1.08x slower                                                                                                    |
| json_dumps           | 16.5 ms                                                                                                           | 18.2 ms: 1.10x slower                                                                                                   |
| pickle_pure_python   | 469 us                                                                                                            | 532 us: 1.14x slower                                                                                                    |
| xml_etree_process    | 78.6 ms                                                                                                           | 98.7 ms: 1.26x slower                                                                                                   |
| json_loads           | 41.3 us                                                                                                           | 52.2 us: 1.26x slower                                                                                                   |
| tomli_loads          | 2.53 sec                                                                                                          | 3.28 sec: 1.29x slower                                                                                                  |
| xml_etree_generate   | 109 ms                                                                                                            | 143 ms: 1.31x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 29.7 ms                                                                                                           | 36.2 ms: 1.22x slower                                                                                                   |
| python_startup_no_site | 17.1 ms                                                                                                           | 22.7 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 50.1 ms                                                                                                           | 56.0 ms: 1.12x slower                                                                                                   |
| genshi_text     | 29.2 ms                                                                                                           | 39.2 ms: 1.34x slower                                                                                                   |
| genshi_xml      | 70.3 ms                                                                                                           | 95.0 ms: 1.35x slower                                                                                                   |
| mako            | 16.3 ms                                                                                                           | 27.3 ms: 1.68x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.36x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles          | 3.51 ms                                                                                                           | 3.09 ms: 1.13x faster                                                                                                   |
| gc_traversal              | 9.75 ms                                                                                                           | 8.84 ms: 1.10x faster                                                                                                   |
| sqlglot_optimize          | 84.3 ms                                                                                                           | 77.5 ms: 1.09x faster                                                                                                   |
| async_tree_io_tg          | 906 ms                                                                                                            | 838 ms: 1.08x faster                                                                                                    |
| coroutines                | 34.7 ms                                                                                                           | 32.3 ms: 1.07x faster                                                                                                   |
| pycparser                 | 1.54 sec                                                                                                          | 1.61 sec: 1.04x slower                                                                                                  |
| sqlite_synth              | 3.57 us                                                                                                           | 3.73 us: 1.04x slower                                                                                                   |
| regex_dna                 | 286 ms                                                                                                            | 301 ms: 1.05x slower                                                                                                    |
| async_tree_none           | 425 ms                                                                                                            | 449 ms: 1.06x slower                                                                                                    |
| k_core                    | 4.27 sec                                                                                                          | 4.57 sec: 1.07x slower                                                                                                  |
| unpickle_pure_python      | 345 us                                                                                                            | 371 us: 1.08x slower                                                                                                    |
| regex_effbot              | 4.20 ms                                                                                                           | 4.53 ms: 1.08x slower                                                                                                   |
| json                      | 7.43 ms                                                                                                           | 8.02 ms: 1.08x slower                                                                                                   |
| scimark_sor               | 177 ms                                                                                                            | 191 ms: 1.08x slower                                                                                                    |
| pidigits                  | 243 ms                                                                                                            | 264 ms: 1.09x slower                                                                                                    |
| docutils                  | 3.90 sec                                                                                                          | 4.25 sec: 1.09x slower                                                                                                  |
| richards                  | 65.9 ms                                                                                                           | 71.9 ms: 1.09x slower                                                                                                   |
| sphinx                    | 1.50 sec                                                                                                          | 1.65 sec: 1.10x slower                                                                                                  |
| async_generators          | 554 ms                                                                                                            | 610 ms: 1.10x slower                                                                                                    |
| json_dumps                | 16.5 ms                                                                                                           | 18.2 ms: 1.10x slower                                                                                                   |
| django_template           | 50.1 ms                                                                                                           | 56.0 ms: 1.12x slower                                                                                                   |
| chaos                     | 90.2 ms                                                                                                           | 101 ms: 1.12x slower                                                                                                    |
| logging_format            | 11.0 us                                                                                                           | 12.4 us: 1.12x slower                                                                                                   |
| nqueens                   | 120 ms                                                                                                            | 135 ms: 1.13x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 727 ms                                                                                                            | 822 ms: 1.13x slower                                                                                                    |
| pickle_pure_python        | 469 us                                                                                                            | 532 us: 1.14x slower                                                                                                    |
| async_tree_memoization_tg | 455 ms                                                                                                            | 517 ms: 1.14x slower                                                                                                    |
| telco                     | 11.9 ms                                                                                                           | 13.5 ms: 1.14x slower                                                                                                   |
| sqlalchemy_declarative    | 211 ms                                                                                                            | 241 ms: 1.14x slower                                                                                                    |
| async_tree_none_tg        | 376 ms                                                                                                            | 429 ms: 1.14x slower                                                                                                    |
| spectral_norm             | 140 ms                                                                                                            | 160 ms: 1.14x slower                                                                                                    |
| scimark_sparse_mat_mult   | 6.54 ms                                                                                                           | 7.51 ms: 1.15x slower                                                                                                   |
| sympy_expand              | 612 ms                                                                                                            | 707 ms: 1.16x slower                                                                                                    |
| asyncio_websockets        | 701 ms                                                                                                            | 811 ms: 1.16x slower                                                                                                    |
| deepcopy_memo             | 43.2 us                                                                                                           | 50.3 us: 1.16x slower                                                                                                   |
| pyflate                   | 708 ms                                                                                                            | 825 ms: 1.17x slower                                                                                                    |
| scimark_fft               | 512 ms                                                                                                            | 597 ms: 1.17x slower                                                                                                    |
| dulwich_log               | 98.7 ms                                                                                                           | 116 ms: 1.17x slower                                                                                                    |
| 2to3                      | 529 ms                                                                                                            | 620 ms: 1.17x slower                                                                                                    |
| shortest_path             | 927 ms                                                                                                            | 1.09 sec: 1.18x slower                                                                                                  |
| thrift                    | 1.13 ms                                                                                                           | 1.33 ms: 1.18x slower                                                                                                   |
| connected_components      | 840 ms                                                                                                            | 994 ms: 1.18x slower                                                                                                    |
| sqlglot_parse             | 1.86 ms                                                                                                           | 2.22 ms: 1.19x slower                                                                                                   |
| regex_compile             | 188 ms                                                                                                            | 224 ms: 1.20x slower                                                                                                    |
| mdp                       | 3.69 sec                                                                                                          | 4.42 sec: 1.20x slower                                                                                                  |
| sympy_str                 | 368 ms                                                                                                            | 443 ms: 1.20x slower                                                                                                    |
| logging_silent            | 150 ns                                                                                                            | 182 ns: 1.21x slower                                                                                                    |
| many_optionals            | 1.40 ms                                                                                                           | 1.69 ms: 1.21x slower                                                                                                   |
| sympy_sum                 | 221 ms                                                                                                            | 268 ms: 1.21x slower                                                                                                    |
| pprint_pformat            | 1.97 sec                                                                                                          | 2.40 sec: 1.22x slower                                                                                                  |
| python_startup            | 29.7 ms                                                                                                           | 36.2 ms: 1.22x slower                                                                                                   |
| pathlib                   | 28.2 ms                                                                                                           | 34.9 ms: 1.23x slower                                                                                                   |
| deepcopy                  | 363 us                                                                                                            | 450 us: 1.24x slower                                                                                                    |
| xml_etree_process         | 78.6 ms                                                                                                           | 98.7 ms: 1.26x slower                                                                                                   |
| json_loads                | 41.3 us                                                                                                           | 52.2 us: 1.26x slower                                                                                                   |
| pylint                    | 399 ms                                                                                                            | 512 ms: 1.28x slower                                                                                                    |
| fannkuch                  | 555 ms                                                                                                            | 712 ms: 1.28x slower                                                                                                    |
| async_tree_memoization    | 491 ms                                                                                                            | 632 ms: 1.29x slower                                                                                                    |
| hexiom                    | 9.34 ms                                                                                                           | 12.1 ms: 1.29x slower                                                                                                   |
| tomli_loads               | 2.53 sec                                                                                                          | 3.28 sec: 1.29x slower                                                                                                  |
| meteor_contest            | 156 ms                                                                                                            | 203 ms: 1.30x slower                                                                                                    |
| pprint_safe_repr          | 904 ms                                                                                                            | 1.18 sec: 1.30x slower                                                                                                  |
| logging_simple            | 9.40 us                                                                                                           | 12.3 us: 1.30x slower                                                                                                   |
| subparsers                | 35.3 ms                                                                                                           | 46.2 ms: 1.31x slower                                                                                                   |
| xml_etree_generate        | 109 ms                                                                                                            | 143 ms: 1.31x slower                                                                                                    |
| generators                | 39.0 ms                                                                                                           | 51.2 ms: 1.31x slower                                                                                                   |
| html5lib                  | 77.2 ms                                                                                                           | 102 ms: 1.32x slower                                                                                                    |
| python_startup_no_site    | 17.1 ms                                                                                                           | 22.7 ms: 1.32x slower                                                                                                   |
| sqlglot_normalize         | 143 ms                                                                                                            | 190 ms: 1.33x slower                                                                                                    |
| scimark_lu                | 154 ms                                                                                                            | 206 ms: 1.34x slower                                                                                                    |
| genshi_text               | 29.2 ms                                                                                                           | 39.2 ms: 1.34x slower                                                                                                   |
| richards_super            | 72.3 ms                                                                                                           | 97.2 ms: 1.34x slower                                                                                                   |
| genshi_xml                | 70.3 ms                                                                                                           | 95.0 ms: 1.35x slower                                                                                                   |
| raytrace                  | 341 ms                                                                                                            | 462 ms: 1.35x slower                                                                                                    |
| bpe_tokeniser             | 6.14 sec                                                                                                          | 8.35 sec: 1.36x slower                                                                                                  |
| comprehensions            | 21.0 us                                                                                                           | 28.8 us: 1.37x slower                                                                                                   |
| deepcopy_reduce           | 3.63 us                                                                                                           | 5.01 us: 1.38x slower                                                                                                   |
| go                        | 158 ms                                                                                                            | 221 ms: 1.40x slower                                                                                                    |
| scimark_monte_carlo       | 91.7 ms                                                                                                           | 129 ms: 1.40x slower                                                                                                    |
| sqlglot_transpile         | 2.38 ms                                                                                                           | 3.40 ms: 1.43x slower                                                                                                   |
| deltablue                 | 4.37 ms                                                                                                           | 6.42 ms: 1.47x slower                                                                                                   |
| nbody                     | 130 ms                                                                                                            | 192 ms: 1.47x slower                                                                                                    |
| typing_runtime_protocols  | 214 us                                                                                                            | 315 us: 1.47x slower                                                                                                    |
| bench_thread_pool         | 3.24 ms                                                                                                           | 5.05 ms: 1.56x slower                                                                                                   |
| sqlalchemy_imperative     | 23.7 ms                                                                                                           | 37.3 ms: 1.57x slower                                                                                                   |
| mako                      | 16.3 ms                                                                                                           | 27.3 ms: 1.68x slower                                                                                                   |
| Geometric mean            | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (10): xml_etree_iterparse, async_tree_io, sympy_integrate, bench_mp_pool, xml_etree_parse, float, async_tree_cpu_io_mixed_tg, crypto_pyaes, regex_v8, coverage

- Geometric mean (including insignificant results): 1.141x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.19x