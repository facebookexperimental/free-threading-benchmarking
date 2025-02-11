# Results vs. base

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.127x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 455 ms                                                                                                            | 542 ms: 1.19x slower                                                                                                    |
| docutils       | 3.70 sec                                                                                                          | 4.14 sec: 1.12x slower                                                                                                  |
| html5lib       | 81.6 ms                                                                                                           | 109 ms: 1.34x slower                                                                                                    |
| sphinx         | 1.39 sec                                                                                                          | 1.65 sec: 1.19x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 934 ms                                                                                                            | 790 ms: 1.18x faster                                                                                                    |
| async_tree_io              | 923 ms                                                                                                            | 842 ms: 1.10x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 700 ms                                                                                                            | 654 ms: 1.07x faster                                                                                                    |
| asyncio_websockets         | 767 ms                                                                                                            | 735 ms: 1.04x faster                                                                                                    |
| async_tree_memoization_tg  | 477 ms                                                                                                            | 460 ms: 1.04x faster                                                                                                    |
| async_generators           | 524 ms                                                                                                            | 558 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 711 ms                                                                                                            | 766 ms: 1.08x slower                                                                                                    |
| coroutines                 | 29.3 ms                                                                                                           | 32.1 ms: 1.10x slower                                                                                                   |
| async_tree_memoization     | 473 ms                                                                                                            | 540 ms: 1.14x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 239 ms                                                                                                            | 231 ms: 1.03x faster                                                                                                    |
| float          | 105 ms                                                                                                            | 114 ms: 1.08x slower                                                                                                    |
| nbody          | 119 ms                                                                                                            | 189 ms: 1.59x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 288 ms                                                                                                            | 269 ms: 1.07x faster                                                                                                    |
| regex_compile  | 166 ms                                                                                                            | 189 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 166 ms                                                                                                            | 151 ms: 1.10x faster                                                                                                    |
| pickle_pure_python   | 424 us                                                                                                            | 450 us: 1.06x slower                                                                                                    |
| json_dumps           | 16.3 ms                                                                                                           | 17.7 ms: 1.09x slower                                                                                                   |
| json_loads           | 38.0 us                                                                                                           | 42.9 us: 1.13x slower                                                                                                   |
| tomli_loads          | 2.57 sec                                                                                                          | 3.03 sec: 1.18x slower                                                                                                  |
| xml_etree_generate   | 115 ms                                                                                                            | 140 ms: 1.22x slower                                                                                                    |
| xml_etree_process    | 77.9 ms                                                                                                           | 96.3 ms: 1.24x slower                                                                                                   |
| unpickle_pure_python | 285 us                                                                                                            | 361 us: 1.27x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 27.0 ms                                                                                                           | 33.0 ms: 1.22x slower                                                                                                   |
| python_startup_no_site | 16.0 ms                                                                                                           | 20.8 ms: 1.30x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                                                                           | 39.0 ms: 1.28x slower                                                                                                   |
| django_template | 43.0 ms                                                                                                           | 56.4 ms: 1.31x slower                                                                                                   |
| genshi_xml      | 62.8 ms                                                                                                           | 95.7 ms: 1.52x slower                                                                                                   |
| mako            | 15.5 ms                                                                                                           | 25.2 ms: 1.62x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.43x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 9.97 ms                                                                                                           | 4.44 ms: 2.24x faster                                                                                                   |
| create_gc_cycles           | 5.09 ms                                                                                                           | 3.11 ms: 1.64x faster                                                                                                   |
| async_tree_io_tg           | 934 ms                                                                                                            | 790 ms: 1.18x faster                                                                                                    |
| xml_etree_iterparse        | 166 ms                                                                                                            | 151 ms: 1.10x faster                                                                                                    |
| async_tree_io              | 923 ms                                                                                                            | 842 ms: 1.10x faster                                                                                                    |
| regex_dna                  | 288 ms                                                                                                            | 269 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 700 ms                                                                                                            | 654 ms: 1.07x faster                                                                                                    |
| asyncio_websockets         | 767 ms                                                                                                            | 735 ms: 1.04x faster                                                                                                    |
| async_tree_memoization_tg  | 477 ms                                                                                                            | 460 ms: 1.04x faster                                                                                                    |
| pidigits                   | 239 ms                                                                                                            | 231 ms: 1.03x faster                                                                                                    |
| pickle_pure_python         | 424 us                                                                                                            | 450 us: 1.06x slower                                                                                                    |
| async_generators           | 524 ms                                                                                                            | 558 ms: 1.07x slower                                                                                                    |
| k_core                     | 4.14 sec                                                                                                          | 4.42 sec: 1.07x slower                                                                                                  |
| pycparser                  | 1.53 sec                                                                                                          | 1.64 sec: 1.07x slower                                                                                                  |
| float                      | 105 ms                                                                                                            | 114 ms: 1.08x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 711 ms                                                                                                            | 766 ms: 1.08x slower                                                                                                    |
| sympy_integrate            | 32.1 ms                                                                                                           | 34.7 ms: 1.08x slower                                                                                                   |
| json                       | 6.77 ms                                                                                                           | 7.34 ms: 1.09x slower                                                                                                   |
| json_dumps                 | 16.3 ms                                                                                                           | 17.7 ms: 1.09x slower                                                                                                   |
| sqlite_synth               | 3.73 us                                                                                                           | 4.08 us: 1.09x slower                                                                                                   |
| coroutines                 | 29.3 ms                                                                                                           | 32.1 ms: 1.10x slower                                                                                                   |
| sqlglot_optimize           | 71.4 ms                                                                                                           | 79.3 ms: 1.11x slower                                                                                                   |
| docutils                   | 3.70 sec                                                                                                          | 4.14 sec: 1.12x slower                                                                                                  |
| sqlglot_normalize          | 140 ms                                                                                                            | 157 ms: 1.12x slower                                                                                                    |
| json_loads                 | 38.0 us                                                                                                           | 42.9 us: 1.13x slower                                                                                                   |
| pyflate                    | 639 ms                                                                                                            | 722 ms: 1.13x slower                                                                                                    |
| scimark_sor                | 154 ms                                                                                                            | 174 ms: 1.13x slower                                                                                                    |
| deepcopy_reduce            | 4.02 us                                                                                                           | 4.56 us: 1.14x slower                                                                                                   |
| raytrace                   | 385 ms                                                                                                            | 437 ms: 1.14x slower                                                                                                    |
| sympy_expand               | 583 ms                                                                                                            | 663 ms: 1.14x slower                                                                                                    |
| deepcopy                   | 340 us                                                                                                            | 387 us: 1.14x slower                                                                                                    |
| regex_compile              | 166 ms                                                                                                            | 189 ms: 1.14x slower                                                                                                    |
| async_tree_memoization     | 473 ms                                                                                                            | 540 ms: 1.14x slower                                                                                                    |
| connected_components       | 803 ms                                                                                                            | 922 ms: 1.15x slower                                                                                                    |
| dulwich_log                | 91.7 ms                                                                                                           | 106 ms: 1.15x slower                                                                                                    |
| thrift                     | 1.10 ms                                                                                                           | 1.27 ms: 1.15x slower                                                                                                   |
| bench_thread_pool          | 3.37 ms                                                                                                           | 3.89 ms: 1.15x slower                                                                                                   |
| sympy_sum                  | 204 ms                                                                                                            | 236 ms: 1.16x slower                                                                                                    |
| go                         | 160 ms                                                                                                            | 188 ms: 1.17x slower                                                                                                    |
| shortest_path              | 908 ms                                                                                                            | 1.07 sec: 1.18x slower                                                                                                  |
| tomli_loads                | 2.57 sec                                                                                                          | 3.03 sec: 1.18x slower                                                                                                  |
| scimark_lu                 | 152 ms                                                                                                            | 179 ms: 1.18x slower                                                                                                    |
| coverage                   | 118 ms                                                                                                            | 140 ms: 1.18x slower                                                                                                    |
| subparsers                 | 32.6 ms                                                                                                           | 38.6 ms: 1.19x slower                                                                                                   |
| pylint                     | 390 ms                                                                                                            | 463 ms: 1.19x slower                                                                                                    |
| mdp                        | 3.53 sec                                                                                                          | 4.20 sec: 1.19x slower                                                                                                  |
| sphinx                     | 1.39 sec                                                                                                          | 1.65 sec: 1.19x slower                                                                                                  |
| 2to3                       | 455 ms                                                                                                            | 542 ms: 1.19x slower                                                                                                    |
| hexiom                     | 8.26 ms                                                                                                           | 9.84 ms: 1.19x slower                                                                                                   |
| nqueens                    | 111 ms                                                                                                            | 133 ms: 1.20x slower                                                                                                    |
| scimark_fft                | 452 ms                                                                                                            | 547 ms: 1.21x slower                                                                                                    |
| many_optionals             | 1.33 ms                                                                                                           | 1.61 ms: 1.21x slower                                                                                                   |
| meteor_contest             | 147 ms                                                                                                            | 179 ms: 1.21x slower                                                                                                    |
| sqlglot_parse              | 1.79 ms                                                                                                           | 2.17 ms: 1.21x slower                                                                                                   |
| generators                 | 40.8 ms                                                                                                           | 49.5 ms: 1.21x slower                                                                                                   |
| xml_etree_generate         | 115 ms                                                                                                            | 140 ms: 1.22x slower                                                                                                    |
| comprehensions             | 20.8 us                                                                                                           | 25.5 us: 1.22x slower                                                                                                   |
| python_startup             | 27.0 ms                                                                                                           | 33.0 ms: 1.22x slower                                                                                                   |
| sqlalchemy_declarative     | 178 ms                                                                                                            | 218 ms: 1.23x slower                                                                                                    |
| logging_simple             | 8.19 us                                                                                                           | 10.1 us: 1.23x slower                                                                                                   |
| xml_etree_process          | 77.9 ms                                                                                                           | 96.3 ms: 1.24x slower                                                                                                   |
| pprint_pformat             | 1.85 sec                                                                                                          | 2.29 sec: 1.24x slower                                                                                                  |
| richards                   | 58.6 ms                                                                                                           | 73.2 ms: 1.25x slower                                                                                                   |
| pprint_safe_repr           | 911 ms                                                                                                            | 1.14 sec: 1.25x slower                                                                                                  |
| logging_format             | 9.48 us                                                                                                           | 11.9 us: 1.25x slower                                                                                                   |
| unpickle_pure_python       | 285 us                                                                                                            | 361 us: 1.27x slower                                                                                                    |
| sqlglot_transpile          | 2.18 ms                                                                                                           | 2.76 ms: 1.27x slower                                                                                                   |
| genshi_text                | 30.6 ms                                                                                                           | 39.0 ms: 1.28x slower                                                                                                   |
| richards_super             | 67.1 ms                                                                                                           | 86.5 ms: 1.29x slower                                                                                                   |
| fannkuch                   | 487 ms                                                                                                            | 630 ms: 1.29x slower                                                                                                    |
| python_startup_no_site     | 16.0 ms                                                                                                           | 20.8 ms: 1.30x slower                                                                                                   |
| telco                      | 9.93 ms                                                                                                           | 12.9 ms: 1.30x slower                                                                                                   |
| scimark_monte_carlo        | 94.4 ms                                                                                                           | 124 ms: 1.31x slower                                                                                                    |
| django_template            | 43.0 ms                                                                                                           | 56.4 ms: 1.31x slower                                                                                                   |
| spectral_norm              | 118 ms                                                                                                            | 157 ms: 1.33x slower                                                                                                    |
| crypto_pyaes               | 89.7 ms                                                                                                           | 120 ms: 1.33x slower                                                                                                    |
| html5lib                   | 81.6 ms                                                                                                           | 109 ms: 1.34x slower                                                                                                    |
| bpe_tokeniser              | 5.67 sec                                                                                                          | 7.60 sec: 1.34x slower                                                                                                  |
| deepcopy_memo              | 38.6 us                                                                                                           | 51.8 us: 1.34x slower                                                                                                   |
| chaos                      | 73.9 ms                                                                                                           | 99.1 ms: 1.34x slower                                                                                                   |
| sympy_str                  | 335 ms                                                                                                            | 454 ms: 1.36x slower                                                                                                    |
| scimark_sparse_mat_mult    | 5.63 ms                                                                                                           | 8.18 ms: 1.45x slower                                                                                                   |
| typing_runtime_protocols   | 199 us                                                                                                            | 289 us: 1.46x slower                                                                                                    |
| sqlalchemy_imperative      | 21.5 ms                                                                                                           | 32.5 ms: 1.51x slower                                                                                                   |
| genshi_xml                 | 62.8 ms                                                                                                           | 95.7 ms: 1.52x slower                                                                                                   |
| deltablue                  | 4.14 ms                                                                                                           | 6.45 ms: 1.56x slower                                                                                                   |
| nbody                      | 119 ms                                                                                                            | 189 ms: 1.59x slower                                                                                                    |
| mako                       | 15.5 ms                                                                                                           | 25.2 ms: 1.62x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (8): bench_mp_pool, xml_etree_parse, regex_v8, async_tree_none_tg, async_tree_none, logging_silent, regex_effbot, pathlib

- Geometric mean (including insignificant results): 1.127x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.19x