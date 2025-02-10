# Results vs. base

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.116x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 438 ms                                                                                                            | 530 ms: 1.21x slower                                                                                                    |
| docutils       | 3.78 sec                                                                                                          | 4.12 sec: 1.09x slower                                                                                                  |
| html5lib       | 83.0 ms                                                                                                           | 93.1 ms: 1.12x slower                                                                                                   |
| sphinx         | 1.44 sec                                                                                                          | 1.60 sec: 1.11x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 919 ms                                                                                                            | 772 ms: 1.19x faster                                                                                                    |
| async_tree_none_tg        | 394 ms                                                                                                            | 348 ms: 1.13x faster                                                                                                    |
| async_tree_io             | 862 ms                                                                                                            | 835 ms: 1.03x faster                                                                                                    |
| async_tree_cpu_io_mixed   | 690 ms                                                                                                            | 734 ms: 1.06x slower                                                                                                    |
| async_tree_memoization_tg | 461 ms                                                                                                            | 496 ms: 1.07x slower                                                                                                    |
| async_tree_none           | 373 ms                                                                                                            | 418 ms: 1.12x slower                                                                                                    |
| async_generators          | 500 ms                                                                                                            | 565 ms: 1.13x slower                                                                                                    |
| async_tree_memoization    | 466 ms                                                                                                            | 528 ms: 1.13x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 123 ms                                                                                                            | 106 ms: 1.16x faster                                                                                                    |
| pidigits       | 240 ms                                                                                                            | 233 ms: 1.03x faster                                                                                                    |
| nbody          | 134 ms                                                                                                            | 179 ms: 1.33x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.28 ms                                                                                                           | 4.49 ms: 1.05x slower                                                                                                   |
| regex_dna      | 275 ms                                                                                                            | 296 ms: 1.08x slower                                                                                                    |
| regex_compile  | 165 ms                                                                                                            | 196 ms: 1.19x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 162 ms                                                                                                            | 137 ms: 1.18x faster                                                                                                    |
| xml_etree_parse      | 202 ms                                                                                                            | 218 ms: 1.08x slower                                                                                                    |
| json_loads           | 37.0 us                                                                                                           | 40.1 us: 1.09x slower                                                                                                   |
| json_dumps           | 15.3 ms                                                                                                           | 17.6 ms: 1.15x slower                                                                                                   |
| pickle_pure_python   | 429 us                                                                                                            | 495 us: 1.15x slower                                                                                                    |
| unpickle_pure_python | 281 us                                                                                                            | 326 us: 1.16x slower                                                                                                    |
| xml_etree_generate   | 116 ms                                                                                                            | 137 ms: 1.18x slower                                                                                                    |
| tomli_loads          | 2.55 sec                                                                                                          | 3.03 sec: 1.19x slower                                                                                                  |
| xml_etree_process    | 75.9 ms                                                                                                           | 99.8 ms: 1.32x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 28.9 ms                                                                                                           | 32.4 ms: 1.12x slower                                                                                                   |
| python_startup_no_site | 16.3 ms                                                                                                           | 19.9 ms: 1.22x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 67.7 ms                                                                                                           | 79.4 ms: 1.17x slower                                                                                                   |
| django_template | 46.8 ms                                                                                                           | 58.4 ms: 1.25x slower                                                                                                   |
| genshi_text     | 29.3 ms                                                                                                           | 40.5 ms: 1.38x slower                                                                                                   |
| mako            | 17.5 ms                                                                                                           | 24.2 ms: 1.39x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.29x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal              | 8.20 ms                                                                                                           | 3.97 ms: 2.07x faster                                                                                                   |
| create_gc_cycles          | 3.71 ms                                                                                                           | 2.78 ms: 1.33x faster                                                                                                   |
| async_tree_io_tg          | 919 ms                                                                                                            | 772 ms: 1.19x faster                                                                                                    |
| xml_etree_iterparse       | 162 ms                                                                                                            | 137 ms: 1.18x faster                                                                                                    |
| float                     | 123 ms                                                                                                            | 106 ms: 1.16x faster                                                                                                    |
| async_tree_none_tg        | 394 ms                                                                                                            | 348 ms: 1.13x faster                                                                                                    |
| bench_mp_pool             | 91.4 ms                                                                                                           | 84.2 ms: 1.08x faster                                                                                                   |
| sqlite_synth              | 3.90 us                                                                                                           | 3.61 us: 1.08x faster                                                                                                   |
| pidigits                  | 240 ms                                                                                                            | 233 ms: 1.03x faster                                                                                                    |
| async_tree_io             | 862 ms                                                                                                            | 835 ms: 1.03x faster                                                                                                    |
| regex_effbot              | 4.28 ms                                                                                                           | 4.49 ms: 1.05x slower                                                                                                   |
| pycparser                 | 1.50 sec                                                                                                          | 1.59 sec: 1.05x slower                                                                                                  |
| pathlib                   | 28.5 ms                                                                                                           | 30.2 ms: 1.06x slower                                                                                                   |
| async_tree_cpu_io_mixed   | 690 ms                                                                                                            | 734 ms: 1.06x slower                                                                                                    |
| k_core                    | 4.19 sec                                                                                                          | 4.46 sec: 1.06x slower                                                                                                  |
| async_tree_memoization_tg | 461 ms                                                                                                            | 496 ms: 1.07x slower                                                                                                    |
| xml_etree_parse           | 202 ms                                                                                                            | 218 ms: 1.08x slower                                                                                                    |
| regex_dna                 | 275 ms                                                                                                            | 296 ms: 1.08x slower                                                                                                    |
| pyflate                   | 667 ms                                                                                                            | 723 ms: 1.08x slower                                                                                                    |
| json_loads                | 37.0 us                                                                                                           | 40.1 us: 1.09x slower                                                                                                   |
| docutils                  | 3.78 sec                                                                                                          | 4.12 sec: 1.09x slower                                                                                                  |
| deepcopy_reduce           | 3.85 us                                                                                                           | 4.22 us: 1.10x slower                                                                                                   |
| sphinx                    | 1.44 sec                                                                                                          | 1.60 sec: 1.11x slower                                                                                                  |
| dulwich_log               | 102 ms                                                                                                            | 114 ms: 1.12x slower                                                                                                    |
| python_startup            | 28.9 ms                                                                                                           | 32.4 ms: 1.12x slower                                                                                                   |
| html5lib                  | 83.0 ms                                                                                                           | 93.1 ms: 1.12x slower                                                                                                   |
| async_tree_none           | 373 ms                                                                                                            | 418 ms: 1.12x slower                                                                                                    |
| sympy_expand              | 603 ms                                                                                                            | 681 ms: 1.13x slower                                                                                                    |
| async_generators          | 500 ms                                                                                                            | 565 ms: 1.13x slower                                                                                                    |
| async_tree_memoization    | 466 ms                                                                                                            | 528 ms: 1.13x slower                                                                                                    |
| json                      | 6.91 ms                                                                                                           | 7.87 ms: 1.14x slower                                                                                                   |
| sympy_str                 | 362 ms                                                                                                            | 414 ms: 1.14x slower                                                                                                    |
| scimark_fft               | 447 ms                                                                                                            | 511 ms: 1.14x slower                                                                                                    |
| json_dumps                | 15.3 ms                                                                                                           | 17.6 ms: 1.15x slower                                                                                                   |
| thrift                    | 1.06 ms                                                                                                           | 1.22 ms: 1.15x slower                                                                                                   |
| pickle_pure_python        | 429 us                                                                                                            | 495 us: 1.15x slower                                                                                                    |
| mdp                       | 3.65 sec                                                                                                          | 4.22 sec: 1.16x slower                                                                                                  |
| generators                | 40.4 ms                                                                                                           | 46.8 ms: 1.16x slower                                                                                                   |
| unpickle_pure_python      | 281 us                                                                                                            | 326 us: 1.16x slower                                                                                                    |
| deepcopy                  | 335 us                                                                                                            | 388 us: 1.16x slower                                                                                                    |
| shortest_path             | 879 ms                                                                                                            | 1.02 sec: 1.16x slower                                                                                                  |
| scimark_lu                | 148 ms                                                                                                            | 172 ms: 1.16x slower                                                                                                    |
| meteor_contest            | 146 ms                                                                                                            | 170 ms: 1.17x slower                                                                                                    |
| pylint                    | 390 ms                                                                                                            | 456 ms: 1.17x slower                                                                                                    |
| genshi_xml                | 67.7 ms                                                                                                           | 79.4 ms: 1.17x slower                                                                                                   |
| xml_etree_generate        | 116 ms                                                                                                            | 137 ms: 1.18x slower                                                                                                    |
| tomli_loads               | 2.55 sec                                                                                                          | 3.03 sec: 1.19x slower                                                                                                  |
| sqlglot_optimize          | 69.7 ms                                                                                                           | 82.8 ms: 1.19x slower                                                                                                   |
| go                        | 155 ms                                                                                                            | 185 ms: 1.19x slower                                                                                                    |
| logging_format            | 9.24 us                                                                                                           | 11.0 us: 1.19x slower                                                                                                   |
| crypto_pyaes              | 92.5 ms                                                                                                           | 110 ms: 1.19x slower                                                                                                    |
| regex_compile             | 165 ms                                                                                                            | 196 ms: 1.19x slower                                                                                                    |
| subparsers                | 32.4 ms                                                                                                           | 38.9 ms: 1.20x slower                                                                                                   |
| sympy_sum                 | 198 ms                                                                                                            | 238 ms: 1.20x slower                                                                                                    |
| spectral_norm             | 125 ms                                                                                                            | 151 ms: 1.20x slower                                                                                                    |
| coverage                  | 118 ms                                                                                                            | 142 ms: 1.20x slower                                                                                                    |
| many_optionals            | 1.30 ms                                                                                                           | 1.57 ms: 1.21x slower                                                                                                   |
| scimark_sor               | 147 ms                                                                                                            | 178 ms: 1.21x slower                                                                                                    |
| 2to3                      | 438 ms                                                                                                            | 530 ms: 1.21x slower                                                                                                    |
| sqlalchemy_imperative     | 23.8 ms                                                                                                           | 28.9 ms: 1.21x slower                                                                                                   |
| sqlglot_transpile         | 2.13 ms                                                                                                           | 2.59 ms: 1.22x slower                                                                                                   |
| sympy_integrate           | 27.0 ms                                                                                                           | 33.0 ms: 1.22x slower                                                                                                   |
| python_startup_no_site    | 16.3 ms                                                                                                           | 19.9 ms: 1.22x slower                                                                                                   |
| sqlalchemy_declarative    | 177 ms                                                                                                            | 217 ms: 1.22x slower                                                                                                    |
| nqueens                   | 104 ms                                                                                                            | 128 ms: 1.23x slower                                                                                                    |
| connected_components      | 793 ms                                                                                                            | 974 ms: 1.23x slower                                                                                                    |
| richards_super            | 67.0 ms                                                                                                           | 82.4 ms: 1.23x slower                                                                                                   |
| telco                     | 9.59 ms                                                                                                           | 11.8 ms: 1.23x slower                                                                                                   |
| deepcopy_memo             | 39.5 us                                                                                                           | 48.7 us: 1.23x slower                                                                                                   |
| comprehensions            | 21.1 us                                                                                                           | 26.1 us: 1.23x slower                                                                                                   |
| pprint_safe_repr          | 915 ms                                                                                                            | 1.13 sec: 1.24x slower                                                                                                  |
| hexiom                    | 8.08 ms                                                                                                           | 10.0 ms: 1.24x slower                                                                                                   |
| pprint_pformat            | 1.85 sec                                                                                                          | 2.30 sec: 1.24x slower                                                                                                  |
| django_template           | 46.8 ms                                                                                                           | 58.4 ms: 1.25x slower                                                                                                   |
| chaos                     | 77.0 ms                                                                                                           | 96.2 ms: 1.25x slower                                                                                                   |
| logging_simple            | 8.10 us                                                                                                           | 10.2 us: 1.26x slower                                                                                                   |
| sqlglot_parse             | 1.80 ms                                                                                                           | 2.27 ms: 1.26x slower                                                                                                   |
| typing_runtime_protocols  | 211 us                                                                                                            | 269 us: 1.27x slower                                                                                                    |
| scimark_sparse_mat_mult   | 6.05 ms                                                                                                           | 7.71 ms: 1.28x slower                                                                                                   |
| richards                  | 58.6 ms                                                                                                           | 75.0 ms: 1.28x slower                                                                                                   |
| raytrace                  | 358 ms                                                                                                            | 459 ms: 1.28x slower                                                                                                    |
| bpe_tokeniser             | 5.61 sec                                                                                                          | 7.25 sec: 1.29x slower                                                                                                  |
| xml_etree_process         | 75.9 ms                                                                                                           | 99.8 ms: 1.32x slower                                                                                                   |
| fannkuch                  | 489 ms                                                                                                            | 645 ms: 1.32x slower                                                                                                    |
| nbody                     | 134 ms                                                                                                            | 179 ms: 1.33x slower                                                                                                    |
| scimark_monte_carlo       | 82.8 ms                                                                                                           | 111 ms: 1.34x slower                                                                                                    |
| genshi_text               | 29.3 ms                                                                                                           | 40.5 ms: 1.38x slower                                                                                                   |
| mako                      | 17.5 ms                                                                                                           | 24.2 ms: 1.39x slower                                                                                                   |
| bench_thread_pool         | 2.77 ms                                                                                                           | 3.94 ms: 1.43x slower                                                                                                   |
| deltablue                 | 4.23 ms                                                                                                           | 6.49 ms: 1.54x slower                                                                                                   |
| Geometric mean            | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (6): logging_silent, async_tree_cpu_io_mixed_tg, regex_v8, asyncio_websockets, coroutines, sqlglot_normalize

- Geometric mean (including insignificant results): 1.116x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x