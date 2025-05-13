# Results vs. base

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 285 ms: 1.14x slower                                                                                                  |
| docutils       | 2.52 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| html5lib       | 61.2 ms                                                                                                         | 67.0 ms: 1.10x slower                                                                                                 |
| sphinx         | 973 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 626 ms                                                                                                          | 523 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 227 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 599 ms                                                                                                          | 551 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 309 ms                                                                                                          | 284 ms: 1.09x faster                                                                                                  |
| async_tree_none            | 271 ms                                                                                                          | 258 ms: 1.05x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                                                          | 485 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 23.2 ms: 1.01x faster                                                                                                 |
| asyncio_websockets         | 518 ms                                                                                                          | 515 ms: 1.00x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                                                          | 509 ms: 1.01x slower                                                                                                  |
| async_generators           | 328 ms                                                                                                          | 371 ms: 1.13x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 70.3 ms                                                                                                         | 70.8 ms: 1.01x slower                                                                                                 |
| pidigits       | 193 ms                                                                                                          | 200 ms: 1.04x slower                                                                                                  |
| nbody          | 87.9 ms                                                                                                         | 120 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.4 ms                                                                                                         | 21.0 ms: 1.07x faster                                                                                                 |
| regex_dna      | 174 ms                                                                                                          | 182 ms: 1.04x slower                                                                                                  |
| regex_effbot   | 2.72 ms                                                                                                         | 2.83 ms: 1.04x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.4 ms                                                                                                         | 86.8 ms: 1.05x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| json_loads           | 28.9 us                                                                                                         | 30.4 us: 1.05x slower                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| json_dumps           | 12.1 ms                                                                                                         | 13.3 ms: 1.09x slower                                                                                                 |
| tomli_loads          | 1.92 sec                                                                                                        | 2.12 sec: 1.11x slower                                                                                                |
| unpickle_pure_python | 207 us                                                                                                          | 230 us: 1.11x slower                                                                                                  |
| xml_etree_generate   | 82.4 ms                                                                                                         | 96.0 ms: 1.17x slower                                                                                                 |
| xml_etree_process    | 57.6 ms                                                                                                         | 68.3 ms: 1.19x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.33 ms                                                                                                         | 9.61 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                                                         | 55.3 ms: 1.16x slower                                                                                                 |
| django_template | 34.2 ms                                                                                                         | 40.7 ms: 1.19x slower                                                                                                 |
| genshi_text     | 20.4 ms                                                                                                         | 25.6 ms: 1.26x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 15.4 ms: 1.29x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.07 ms                                                                                                         | 1.93 ms: 2.11x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.51 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 626 ms                                                                                                          | 523 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 227 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 599 ms                                                                                                          | 551 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 309 ms                                                                                                          | 284 ms: 1.09x faster                                                                                                  |
| sqlite_synth               | 2.25 us                                                                                                         | 2.08 us: 1.08x faster                                                                                                 |
| regex_v8                   | 22.4 ms                                                                                                         | 21.0 ms: 1.07x faster                                                                                                 |
| xml_etree_iterparse        | 91.4 ms                                                                                                         | 86.8 ms: 1.05x faster                                                                                                 |
| async_tree_none            | 271 ms                                                                                                          | 258 ms: 1.05x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                                                          | 485 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 132 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| json                       | 5.19 ms                                                                                                         | 5.14 ms: 1.01x faster                                                                                                 |
| coroutines                 | 23.4 ms                                                                                                         | 23.2 ms: 1.01x faster                                                                                                 |
| asyncio_websockets         | 518 ms                                                                                                          | 515 ms: 1.00x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                                                          | 509 ms: 1.01x slower                                                                                                  |
| float                      | 70.3 ms                                                                                                         | 70.8 ms: 1.01x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.13 sec: 1.03x slower                                                                                                |
| pidigits                   | 193 ms                                                                                                          | 200 ms: 1.04x slower                                                                                                  |
| regex_dna                  | 174 ms                                                                                                          | 182 ms: 1.04x slower                                                                                                  |
| regex_effbot               | 2.72 ms                                                                                                         | 2.83 ms: 1.04x slower                                                                                                 |
| bench_mp_pool              | 98.7 ms                                                                                                         | 103 ms: 1.04x slower                                                                                                  |
| dulwich_log                | 67.8 ms                                                                                                         | 71.2 ms: 1.05x slower                                                                                                 |
| json_loads                 | 28.9 us                                                                                                         | 30.4 us: 1.05x slower                                                                                                 |
| docutils                   | 2.52 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| bpe_tokeniser              | 4.08 sec                                                                                                        | 4.39 sec: 1.08x slower                                                                                                |
| many_optionals             | 1.06 ms                                                                                                         | 1.15 ms: 1.08x slower                                                                                                 |
| pickle_pure_python         | 306 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| pprint_safe_repr           | 708 ms                                                                                                          | 773 ms: 1.09x slower                                                                                                  |
| json_dumps                 | 12.1 ms                                                                                                         | 13.3 ms: 1.09x slower                                                                                                 |
| html5lib                   | 61.2 ms                                                                                                         | 67.0 ms: 1.10x slower                                                                                                 |
| generators                 | 26.8 ms                                                                                                         | 29.4 ms: 1.10x slower                                                                                                 |
| sphinx                     | 973 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| pylint                     | 278 ms                                                                                                          | 306 ms: 1.10x slower                                                                                                  |
| deltablue                  | 3.21 ms                                                                                                         | 3.54 ms: 1.10x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| nqueens                    | 78.6 ms                                                                                                         | 86.9 ms: 1.11x slower                                                                                                 |
| tomli_loads                | 1.92 sec                                                                                                        | 2.12 sec: 1.11x slower                                                                                                |
| pprint_pformat             | 1.45 sec                                                                                                        | 1.61 sec: 1.11x slower                                                                                                |
| unpickle_pure_python       | 207 us                                                                                                          | 230 us: 1.11x slower                                                                                                  |
| scimark_sor                | 110 ms                                                                                                          | 122 ms: 1.11x slower                                                                                                  |
| chaos                      | 55.3 ms                                                                                                         | 61.7 ms: 1.12x slower                                                                                                 |
| scimark_fft                | 326 ms                                                                                                          | 365 ms: 1.12x slower                                                                                                  |
| subparsers                 | 25.3 ms                                                                                                         | 28.5 ms: 1.13x slower                                                                                                 |
| spectral_norm              | 96.3 ms                                                                                                         | 109 ms: 1.13x slower                                                                                                  |
| deepcopy_reduce            | 2.65 us                                                                                                         | 3.00 us: 1.13x slower                                                                                                 |
| async_generators           | 328 ms                                                                                                          | 371 ms: 1.13x slower                                                                                                  |
| 2to3                       | 249 ms                                                                                                          | 285 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.6 ms                                                                                                         | 57.2 ms: 1.15x slower                                                                                                 |
| go                         | 107 ms                                                                                                          | 123 ms: 1.15x slower                                                                                                  |
| telco                      | 7.49 ms                                                                                                         | 8.66 ms: 1.16x slower                                                                                                 |
| genshi_xml                 | 47.8 ms                                                                                                         | 55.3 ms: 1.16x slower                                                                                                 |
| hexiom                     | 5.67 ms                                                                                                         | 6.58 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 250 us                                                                                                          | 291 us: 1.16x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.16x slower                                                                                                |
| logging_silent             | 465 ns                                                                                                          | 541 ns: 1.16x slower                                                                                                  |
| xml_etree_generate         | 82.4 ms                                                                                                         | 96.0 ms: 1.17x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.7 ms                                                                                                         | 115 ms: 1.17x slower                                                                                                  |
| regex_compile              | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| sympy_sum                  | 153 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| sympy_expand               | 455 ms                                                                                                          | 536 ms: 1.18x slower                                                                                                  |
| comprehensions             | 16.5 us                                                                                                         | 19.5 us: 1.18x slower                                                                                                 |
| logging_format             | 7.44 us                                                                                                         | 8.78 us: 1.18x slower                                                                                                 |
| sympy_str                  | 268 ms                                                                                                          | 317 ms: 1.18x slower                                                                                                  |
| thrift                     | 737 us                                                                                                          | 871 us: 1.18x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.2 ms: 1.18x slower                                                                                                 |
| raytrace                   | 251 ms                                                                                                          | 297 ms: 1.19x slower                                                                                                  |
| xml_etree_process          | 57.6 ms                                                                                                         | 68.3 ms: 1.19x slower                                                                                                 |
| django_template            | 34.2 ms                                                                                                         | 40.7 ms: 1.19x slower                                                                                                 |
| logging_simple             | 6.54 us                                                                                                         | 7.81 us: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.80 ms: 1.19x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.45 ms: 1.20x slower                                                                                                 |
| pyflate                    | 398 ms                                                                                                          | 481 ms: 1.21x slower                                                                                                  |
| fannkuch                   | 385 ms                                                                                                          | 467 ms: 1.21x slower                                                                                                  |
| crypto_pyaes               | 69.5 ms                                                                                                         | 84.7 ms: 1.22x slower                                                                                                 |
| scimark_lu                 | 108 ms                                                                                                          | 132 ms: 1.22x slower                                                                                                  |
| shortest_path              | 432 ms                                                                                                          | 529 ms: 1.22x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.52 ms                                                                                                         | 5.53 ms: 1.22x slower                                                                                                 |
| scimark_monte_carlo        | 62.2 ms                                                                                                         | 76.5 ms: 1.23x slower                                                                                                 |
| connected_components       | 391 ms                                                                                                          | 482 ms: 1.23x slower                                                                                                  |
| deepcopy_memo              | 28.5 us                                                                                                         | 35.6 us: 1.25x slower                                                                                                 |
| genshi_text                | 20.4 ms                                                                                                         | 25.6 ms: 1.26x slower                                                                                                 |
| typing_runtime_protocols   | 154 us                                                                                                          | 196 us: 1.27x slower                                                                                                  |
| richards_super             | 45.7 ms                                                                                                         | 58.0 ms: 1.27x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| richards                   | 39.8 ms                                                                                                         | 50.7 ms: 1.27x slower                                                                                                 |
| mako                       | 11.9 ms                                                                                                         | 15.4 ms: 1.29x slower                                                                                                 |
| meteor_contest             | 99.7 ms                                                                                                         | 129 ms: 1.30x slower                                                                                                  |
| python_startup_no_site     | 7.33 ms                                                                                                         | 9.61 ms: 1.31x slower                                                                                                 |
| coverage                   | 82.0 ms                                                                                                         | 109 ms: 1.33x slower                                                                                                  |
| nbody                      | 87.9 ms                                                                                                         | 120 ms: 1.37x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.12 ms: 2.97x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, pathlib

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.23x