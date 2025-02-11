# Results vs. base

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.136x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 305 ms: 1.21x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 2.84 sec: 1.11x slower                                                                                                  |
| sphinx         | 976 ms                                                                                                            | 1.12 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 630 ms                                                                                                            | 579 ms: 1.09x faster                                                                                                    |
| async_tree_io              | 623 ms                                                                                                            | 612 ms: 1.02x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                                                            | 504 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                            | 533 ms: 1.07x slower                                                                                                    |
| async_tree_none            | 269 ms                                                                                                            | 291 ms: 1.08x slower                                                                                                    |
| coroutines                 | 21.4 ms                                                                                                           | 23.4 ms: 1.09x slower                                                                                                   |
| async_tree_memoization     | 321 ms                                                                                                            | 355 ms: 1.11x slower                                                                                                    |
| async_generators           | 325 ms                                                                                                            | 370 ms: 1.14x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                            | 195 ms: 1.04x slower                                                                                                    |
| float          | 70.0 ms                                                                                                           | 76.6 ms: 1.09x slower                                                                                                   |
| nbody          | 89.8 ms                                                                                                           | 132 ms: 1.47x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.3 ms                                                                                                           | 23.9 ms: 1.02x slower                                                                                                   |
| regex_effbot   | 2.73 ms                                                                                                           | 2.84 ms: 1.04x slower                                                                                                   |
| regex_dna      | 164 ms                                                                                                            | 182 ms: 1.11x slower                                                                                                    |
| regex_compile  | 126 ms                                                                                                            | 152 ms: 1.21x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.1 ms                                                                                                           | 87.7 ms: 1.04x faster                                                                                                   |
| xml_etree_parse      | 129 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| json_loads           | 28.6 us                                                                                                           | 31.5 us: 1.10x slower                                                                                                   |
| json_dumps           | 11.5 ms                                                                                                           | 12.8 ms: 1.11x slower                                                                                                   |
| xml_etree_generate   | 82.6 ms                                                                                                           | 96.7 ms: 1.17x slower                                                                                                   |
| unpickle_pure_python | 212 us                                                                                                            | 248 us: 1.17x slower                                                                                                    |
| pickle_pure_python   | 311 us                                                                                                            | 369 us: 1.19x slower                                                                                                    |
| xml_etree_process    | 57.6 ms                                                                                                           | 68.6 ms: 1.19x slower                                                                                                   |
| tomli_loads          | 1.90 sec                                                                                                          | 2.34 sec: 1.23x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.4 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 7.47 ms                                                                                                           | 9.62 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                                                           | 42.3 ms: 1.23x slower                                                                                                   |
| genshi_xml      | 47.0 ms                                                                                                           | 59.7 ms: 1.27x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 15.7 ms: 1.33x slower                                                                                                   |
| genshi_text     | 20.9 ms                                                                                                           | 27.9 ms: 1.33x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.29x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json | results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.25 ms                                                                                                           | 1.72 ms: 2.46x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.37 ms: 1.35x faster                                                                                                   |
| async_tree_io_tg           | 630 ms                                                                                                            | 579 ms: 1.09x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.03 us: 1.08x faster                                                                                                   |
| xml_etree_iterparse        | 91.1 ms                                                                                                           | 87.7 ms: 1.04x faster                                                                                                   |
| async_tree_io              | 623 ms                                                                                                            | 612 ms: 1.02x faster                                                                                                    |
| xml_etree_parse            | 129 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| regex_v8                   | 23.3 ms                                                                                                           | 23.9 ms: 1.02x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                                                            | 504 ms: 1.03x slower                                                                                                    |
| pathlib                    | 18.7 ms                                                                                                           | 19.4 ms: 1.04x slower                                                                                                   |
| regex_effbot               | 2.73 ms                                                                                                           | 2.84 ms: 1.04x slower                                                                                                   |
| pidigits                   | 187 ms                                                                                                            | 195 ms: 1.04x slower                                                                                                    |
| python_startup             | 14.7 ms                                                                                                           | 15.4 ms: 1.05x slower                                                                                                   |
| json                       | 5.13 ms                                                                                                           | 5.43 ms: 1.06x slower                                                                                                   |
| pycparser                  | 1.11 sec                                                                                                          | 1.18 sec: 1.06x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                            | 533 ms: 1.07x slower                                                                                                    |
| bench_mp_pool              | 88.5 ms                                                                                                           | 95.1 ms: 1.07x slower                                                                                                   |
| async_tree_none            | 269 ms                                                                                                            | 291 ms: 1.08x slower                                                                                                    |
| generators                 | 28.9 ms                                                                                                           | 31.4 ms: 1.09x slower                                                                                                   |
| coroutines                 | 21.4 ms                                                                                                           | 23.4 ms: 1.09x slower                                                                                                   |
| float                      | 70.0 ms                                                                                                           | 76.6 ms: 1.09x slower                                                                                                   |
| dulwich_log                | 75.4 ms                                                                                                           | 82.7 ms: 1.10x slower                                                                                                   |
| logging_silent             | 104 ns                                                                                                            | 114 ns: 1.10x slower                                                                                                    |
| json_loads                 | 28.6 us                                                                                                           | 31.5 us: 1.10x slower                                                                                                   |
| mdp                        | 2.45 sec                                                                                                          | 2.70 sec: 1.10x slower                                                                                                  |
| async_tree_memoization     | 321 ms                                                                                                            | 355 ms: 1.11x slower                                                                                                    |
| regex_dna                  | 164 ms                                                                                                            | 182 ms: 1.11x slower                                                                                                    |
| docutils                   | 2.55 sec                                                                                                          | 2.84 sec: 1.11x slower                                                                                                  |
| json_dumps                 | 11.5 ms                                                                                                           | 12.8 ms: 1.11x slower                                                                                                   |
| k_core                     | 2.06 sec                                                                                                          | 2.32 sec: 1.13x slower                                                                                                  |
| bpe_tokeniser              | 4.14 sec                                                                                                          | 4.67 sec: 1.13x slower                                                                                                  |
| async_generators           | 325 ms                                                                                                            | 370 ms: 1.14x slower                                                                                                    |
| pylint                     | 277 ms                                                                                                            | 317 ms: 1.14x slower                                                                                                    |
| sphinx                     | 976 ms                                                                                                            | 1.12 sec: 1.14x slower                                                                                                  |
| subparsers                 | 22.2 ms                                                                                                           | 25.4 ms: 1.14x slower                                                                                                   |
| many_optionals             | 1.02 ms                                                                                                           | 1.18 ms: 1.16x slower                                                                                                   |
| xml_etree_generate         | 82.6 ms                                                                                                           | 96.7 ms: 1.17x slower                                                                                                   |
| unpickle_pure_python       | 212 us                                                                                                            | 248 us: 1.17x slower                                                                                                    |
| telco                      | 7.36 ms                                                                                                           | 8.63 ms: 1.17x slower                                                                                                   |
| sqlglot_normalize          | 101 ms                                                                                                            | 120 ms: 1.18x slower                                                                                                    |
| spectral_norm              | 91.1 ms                                                                                                           | 108 ms: 1.19x slower                                                                                                    |
| pickle_pure_python         | 311 us                                                                                                            | 369 us: 1.19x slower                                                                                                    |
| pprint_safe_repr           | 693 ms                                                                                                            | 825 ms: 1.19x slower                                                                                                    |
| scimark_lu                 | 113 ms                                                                                                            | 135 ms: 1.19x slower                                                                                                    |
| xml_etree_process          | 57.6 ms                                                                                                           | 68.6 ms: 1.19x slower                                                                                                   |
| sqlglot_optimize           | 51.0 ms                                                                                                           | 61.0 ms: 1.20x slower                                                                                                   |
| scimark_sor                | 112 ms                                                                                                            | 134 ms: 1.20x slower                                                                                                    |
| pprint_pformat             | 1.41 sec                                                                                                          | 1.70 sec: 1.21x slower                                                                                                  |
| scimark_fft                | 319 ms                                                                                                            | 385 ms: 1.21x slower                                                                                                    |
| 2to3                       | 252 ms                                                                                                            | 305 ms: 1.21x slower                                                                                                    |
| regex_compile              | 126 ms                                                                                                            | 152 ms: 1.21x slower                                                                                                    |
| nqueens                    | 78.2 ms                                                                                                           | 95.4 ms: 1.22x slower                                                                                                   |
| logging_simple             | 5.92 us                                                                                                           | 7.22 us: 1.22x slower                                                                                                   |
| comprehensions             | 16.3 us                                                                                                           | 20.0 us: 1.23x slower                                                                                                   |
| sympy_expand               | 450 ms                                                                                                            | 552 ms: 1.23x slower                                                                                                    |
| thrift                     | 741 us                                                                                                            | 908 us: 1.23x slower                                                                                                    |
| deepcopy                   | 252 us                                                                                                            | 309 us: 1.23x slower                                                                                                    |
| coverage                   | 78.8 ms                                                                                                           | 96.8 ms: 1.23x slower                                                                                                   |
| sqlalchemy_declarative     | 127 ms                                                                                                            | 156 ms: 1.23x slower                                                                                                    |
| deepcopy_reduce            | 2.60 us                                                                                                           | 3.19 us: 1.23x slower                                                                                                   |
| tomli_loads                | 1.90 sec                                                                                                          | 2.34 sec: 1.23x slower                                                                                                  |
| sympy_integrate            | 19.6 ms                                                                                                           | 24.1 ms: 1.23x slower                                                                                                   |
| go                         | 114 ms                                                                                                            | 140 ms: 1.23x slower                                                                                                    |
| django_template            | 34.2 ms                                                                                                           | 42.3 ms: 1.23x slower                                                                                                   |
| sympy_sum                  | 151 ms                                                                                                            | 186 ms: 1.24x slower                                                                                                    |
| sqlglot_transpile          | 1.53 ms                                                                                                           | 1.90 ms: 1.24x slower                                                                                                   |
| pyflate                    | 410 ms                                                                                                            | 509 ms: 1.24x slower                                                                                                    |
| chaos                      | 55.6 ms                                                                                                           | 69.2 ms: 1.24x slower                                                                                                   |
| logging_format             | 6.63 us                                                                                                           | 8.32 us: 1.26x slower                                                                                                   |
| connected_components       | 395 ms                                                                                                            | 499 ms: 1.26x slower                                                                                                    |
| sympy_str                  | 267 ms                                                                                                            | 338 ms: 1.27x slower                                                                                                    |
| hexiom                     | 5.87 ms                                                                                                           | 7.44 ms: 1.27x slower                                                                                                   |
| shortest_path              | 431 ms                                                                                                            | 548 ms: 1.27x slower                                                                                                    |
| genshi_xml                 | 47.0 ms                                                                                                           | 59.7 ms: 1.27x slower                                                                                                   |
| sqlglot_parse              | 1.23 ms                                                                                                           | 1.58 ms: 1.28x slower                                                                                                   |
| raytrace                   | 256 ms                                                                                                            | 330 ms: 1.29x slower                                                                                                    |
| python_startup_no_site     | 7.47 ms                                                                                                           | 9.62 ms: 1.29x slower                                                                                                   |
| deepcopy_memo              | 29.8 us                                                                                                           | 38.4 us: 1.29x slower                                                                                                   |
| sqlalchemy_imperative      | 19.0 ms                                                                                                           | 24.6 ms: 1.29x slower                                                                                                   |
| scimark_monte_carlo        | 62.8 ms                                                                                                           | 82.3 ms: 1.31x slower                                                                                                   |
| typing_runtime_protocols   | 152 us                                                                                                            | 200 us: 1.32x slower                                                                                                    |
| crypto_pyaes               | 65.6 ms                                                                                                           | 87.3 ms: 1.33x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.24 ms                                                                                                           | 5.65 ms: 1.33x slower                                                                                                   |
| mako                       | 11.8 ms                                                                                                           | 15.7 ms: 1.33x slower                                                                                                   |
| genshi_text                | 20.9 ms                                                                                                           | 27.9 ms: 1.33x slower                                                                                                   |
| fannkuch                   | 368 ms                                                                                                            | 493 ms: 1.34x slower                                                                                                    |
| meteor_contest             | 96.7 ms                                                                                                           | 130 ms: 1.34x slower                                                                                                    |
| richards                   | 41.5 ms                                                                                                           | 56.6 ms: 1.36x slower                                                                                                   |
| richards_super             | 47.5 ms                                                                                                           | 65.7 ms: 1.38x slower                                                                                                   |
| nbody                      | 89.8 ms                                                                                                           | 132 ms: 1.47x slower                                                                                                    |
| deltablue                  | 3.10 ms                                                                                                           | 4.74 ms: 1.53x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.33 ms: 3.24x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: html5lib

- Geometric mean (including insignificant results): 1.136x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x