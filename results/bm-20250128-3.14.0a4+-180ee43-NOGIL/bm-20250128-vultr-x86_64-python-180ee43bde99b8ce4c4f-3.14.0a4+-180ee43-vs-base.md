# Results vs. base

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.157x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                                                            | 313 ms: 1.24x slower                                                                                                    |
| docutils       | 2.56 sec                                                                                                          | 2.87 sec: 1.12x slower                                                                                                  |
| sphinx         | 981 ms                                                                                                            | 1.14 sec: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 623 ms                                                                                                            | 590 ms: 1.06x faster                                                                                                    |
| async_tree_none_tg         | 263 ms                                                                                                            | 256 ms: 1.03x faster                                                                                                    |
| async_tree_memoization_tg  | 316 ms                                                                                                            | 327 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 514 ms: 1.06x slower                                                                                                    |
| async_tree_none            | 271 ms                                                                                                            | 296 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                            | 547 ms: 1.10x slower                                                                                                    |
| async_tree_memoization     | 322 ms                                                                                                            | 362 ms: 1.12x slower                                                                                                    |
| coroutines                 | 21.7 ms                                                                                                           | 24.8 ms: 1.14x slower                                                                                                   |
| async_generators           | 325 ms                                                                                                            | 378 ms: 1.16x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_io, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 200 ms                                                                                                            | 191 ms: 1.05x faster                                                                                                    |
| float          | 72.5 ms                                                                                                           | 78.3 ms: 1.08x slower                                                                                                   |
| nbody          | 88.0 ms                                                                                                           | 141 ms: 1.60x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.7 ms                                                                                                           | 24.1 ms: 1.02x slower                                                                                                   |
| regex_effbot   | 2.76 ms                                                                                                           | 2.87 ms: 1.04x slower                                                                                                   |
| regex_dna      | 169 ms                                                                                                            | 185 ms: 1.09x slower                                                                                                    |
| regex_compile  | 126 ms                                                                                                            | 157 ms: 1.25x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                                                           | 88.1 ms: 1.03x faster                                                                                                   |
| xml_etree_parse      | 126 ms                                                                                                            | 129 ms: 1.02x slower                                                                                                    |
| json_loads           | 28.7 us                                                                                                           | 31.4 us: 1.09x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 13.1 ms: 1.17x slower                                                                                                   |
| xml_etree_generate   | 83.3 ms                                                                                                           | 98.2 ms: 1.18x slower                                                                                                   |
| unpickle_pure_python | 212 us                                                                                                            | 258 us: 1.22x slower                                                                                                    |
| xml_etree_process    | 58.4 ms                                                                                                           | 71.2 ms: 1.22x slower                                                                                                   |
| pickle_pure_python   | 313 us                                                                                                            | 387 us: 1.24x slower                                                                                                    |
| tomli_loads          | 1.92 sec                                                                                                          | 2.42 sec: 1.26x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                                                           | 15.2 ms: 1.04x slower                                                                                                   |
| python_startup_no_site | 7.41 ms                                                                                                           | 9.55 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                                                           | 45.1 ms: 1.29x slower                                                                                                   |
| genshi_xml      | 48.3 ms                                                                                                           | 62.6 ms: 1.30x slower                                                                                                   |
| genshi_text     | 21.0 ms                                                                                                           | 28.7 ms: 1.36x slower                                                                                                   |
| mako            | 11.6 ms                                                                                                           | 16.3 ms: 1.40x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.34x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json | results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 1.85 ms                                                                                                           | 1.32 ms: 1.40x faster                                                                                                   |
| gc_traversal               | 4.37 ms                                                                                                           | 3.35 ms: 1.31x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.06 us: 1.07x faster                                                                                                   |
| async_tree_io_tg           | 623 ms                                                                                                            | 590 ms: 1.06x faster                                                                                                    |
| pidigits                   | 200 ms                                                                                                            | 191 ms: 1.05x faster                                                                                                    |
| xml_etree_iterparse        | 90.5 ms                                                                                                           | 88.1 ms: 1.03x faster                                                                                                   |
| async_tree_none_tg         | 263 ms                                                                                                            | 256 ms: 1.03x faster                                                                                                    |
| regex_v8                   | 23.7 ms                                                                                                           | 24.1 ms: 1.02x slower                                                                                                   |
| xml_etree_parse            | 126 ms                                                                                                            | 129 ms: 1.02x slower                                                                                                    |
| async_tree_memoization_tg  | 316 ms                                                                                                            | 327 ms: 1.03x slower                                                                                                    |
| regex_effbot               | 2.76 ms                                                                                                           | 2.87 ms: 1.04x slower                                                                                                   |
| python_startup             | 14.6 ms                                                                                                           | 15.2 ms: 1.04x slower                                                                                                   |
| pathlib                    | 18.0 ms                                                                                                           | 19.1 ms: 1.06x slower                                                                                                   |
| json                       | 5.07 ms                                                                                                           | 5.37 ms: 1.06x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 514 ms: 1.06x slower                                                                                                    |
| bench_mp_pool              | 88.1 ms                                                                                                           | 95.1 ms: 1.08x slower                                                                                                   |
| float                      | 72.5 ms                                                                                                           | 78.3 ms: 1.08x slower                                                                                                   |
| regex_dna                  | 169 ms                                                                                                            | 185 ms: 1.09x slower                                                                                                    |
| json_loads                 | 28.7 us                                                                                                           | 31.4 us: 1.09x slower                                                                                                   |
| async_tree_none            | 271 ms                                                                                                            | 296 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                            | 547 ms: 1.10x slower                                                                                                    |
| pycparser                  | 1.11 sec                                                                                                          | 1.23 sec: 1.11x slower                                                                                                  |
| mdp                        | 2.47 sec                                                                                                          | 2.73 sec: 1.11x slower                                                                                                  |
| dulwich_log                | 75.1 ms                                                                                                           | 84.2 ms: 1.12x slower                                                                                                   |
| docutils                   | 2.56 sec                                                                                                          | 2.87 sec: 1.12x slower                                                                                                  |
| async_tree_memoization     | 322 ms                                                                                                            | 362 ms: 1.12x slower                                                                                                    |
| bpe_tokeniser              | 4.22 sec                                                                                                          | 4.76 sec: 1.13x slower                                                                                                  |
| logging_silent             | 103 ns                                                                                                            | 118 ns: 1.14x slower                                                                                                    |
| k_core                     | 2.05 sec                                                                                                          | 2.34 sec: 1.14x slower                                                                                                  |
| coroutines                 | 21.7 ms                                                                                                           | 24.8 ms: 1.14x slower                                                                                                   |
| generators                 | 28.9 ms                                                                                                           | 33.4 ms: 1.15x slower                                                                                                   |
| sphinx                     | 981 ms                                                                                                            | 1.14 sec: 1.16x slower                                                                                                  |
| async_generators           | 325 ms                                                                                                            | 378 ms: 1.16x slower                                                                                                    |
| pylint                     | 279 ms                                                                                                            | 326 ms: 1.17x slower                                                                                                    |
| json_dumps                 | 11.2 ms                                                                                                           | 13.1 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 83.3 ms                                                                                                           | 98.2 ms: 1.18x slower                                                                                                   |
| many_optionals             | 1.02 ms                                                                                                           | 1.21 ms: 1.18x slower                                                                                                   |
| subparsers                 | 21.9 ms                                                                                                           | 26.0 ms: 1.19x slower                                                                                                   |
| sqlglot_normalize          | 104 ms                                                                                                            | 125 ms: 1.20x slower                                                                                                    |
| telco                      | 7.14 ms                                                                                                           | 8.64 ms: 1.21x slower                                                                                                   |
| sqlglot_optimize           | 52.1 ms                                                                                                           | 63.1 ms: 1.21x slower                                                                                                   |
| unpickle_pure_python       | 212 us                                                                                                            | 258 us: 1.22x slower                                                                                                    |
| pyflate                    | 414 ms                                                                                                            | 504 ms: 1.22x slower                                                                                                    |
| xml_etree_process          | 58.4 ms                                                                                                           | 71.2 ms: 1.22x slower                                                                                                   |
| pprint_safe_repr           | 705 ms                                                                                                            | 861 ms: 1.22x slower                                                                                                    |
| sympy_expand               | 459 ms                                                                                                            | 565 ms: 1.23x slower                                                                                                    |
| scimark_sor                | 114 ms                                                                                                            | 140 ms: 1.23x slower                                                                                                    |
| spectral_norm              | 92.6 ms                                                                                                           | 114 ms: 1.23x slower                                                                                                    |
| pickle_pure_python         | 313 us                                                                                                            | 387 us: 1.24x slower                                                                                                    |
| pprint_pformat             | 1.43 sec                                                                                                          | 1.77 sec: 1.24x slower                                                                                                  |
| 2to3                       | 253 ms                                                                                                            | 313 ms: 1.24x slower                                                                                                    |
| logging_simple             | 6.03 us                                                                                                           | 7.47 us: 1.24x slower                                                                                                   |
| coverage                   | 79.6 ms                                                                                                           | 99.0 ms: 1.24x slower                                                                                                   |
| sympy_sum                  | 153 ms                                                                                                            | 190 ms: 1.25x slower                                                                                                    |
| nqueens                    | 78.2 ms                                                                                                           | 97.6 ms: 1.25x slower                                                                                                   |
| regex_compile              | 126 ms                                                                                                            | 157 ms: 1.25x slower                                                                                                    |
| sympy_integrate            | 19.8 ms                                                                                                           | 24.7 ms: 1.25x slower                                                                                                   |
| go                         | 115 ms                                                                                                            | 144 ms: 1.25x slower                                                                                                    |
| thrift                     | 732 us                                                                                                            | 920 us: 1.26x slower                                                                                                    |
| tomli_loads                | 1.92 sec                                                                                                          | 2.42 sec: 1.26x slower                                                                                                  |
| shortest_path              | 433 ms                                                                                                            | 546 ms: 1.26x slower                                                                                                    |
| deepcopy                   | 256 us                                                                                                            | 324 us: 1.26x slower                                                                                                    |
| sympy_str                  | 271 ms                                                                                                            | 343 ms: 1.26x slower                                                                                                    |
| connected_components       | 391 ms                                                                                                            | 495 ms: 1.27x slower                                                                                                    |
| sqlalchemy_declarative     | 127 ms                                                                                                            | 161 ms: 1.27x slower                                                                                                    |
| logging_format             | 6.75 us                                                                                                           | 8.54 us: 1.27x slower                                                                                                   |
| sqlalchemy_imperative      | 19.1 ms                                                                                                           | 24.3 ms: 1.27x slower                                                                                                   |
| comprehensions             | 16.7 us                                                                                                           | 21.3 us: 1.28x slower                                                                                                   |
| sqlglot_transpile          | 1.54 ms                                                                                                           | 1.97 ms: 1.28x slower                                                                                                   |
| deepcopy_reduce            | 2.63 us                                                                                                           | 3.38 us: 1.28x slower                                                                                                   |
| scimark_fft                | 310 ms                                                                                                            | 399 ms: 1.29x slower                                                                                                    |
| django_template            | 35.1 ms                                                                                                           | 45.1 ms: 1.29x slower                                                                                                   |
| python_startup_no_site     | 7.41 ms                                                                                                           | 9.55 ms: 1.29x slower                                                                                                   |
| chaos                      | 55.7 ms                                                                                                           | 72.0 ms: 1.29x slower                                                                                                   |
| scimark_lu                 | 111 ms                                                                                                            | 143 ms: 1.29x slower                                                                                                    |
| raytrace                   | 263 ms                                                                                                            | 340 ms: 1.30x slower                                                                                                    |
| genshi_xml                 | 48.3 ms                                                                                                           | 62.6 ms: 1.30x slower                                                                                                   |
| typing_runtime_protocols   | 157 us                                                                                                            | 207 us: 1.32x slower                                                                                                    |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.64 ms: 1.32x slower                                                                                                   |
| deepcopy_memo              | 29.9 us                                                                                                           | 39.5 us: 1.32x slower                                                                                                   |
| fannkuch                   | 371 ms                                                                                                            | 491 ms: 1.33x slower                                                                                                    |
| scimark_monte_carlo        | 64.3 ms                                                                                                           | 85.3 ms: 1.33x slower                                                                                                   |
| hexiom                     | 5.70 ms                                                                                                           | 7.62 ms: 1.34x slower                                                                                                   |
| meteor_contest             | 97.7 ms                                                                                                           | 132 ms: 1.35x slower                                                                                                    |
| crypto_pyaes               | 65.9 ms                                                                                                           | 89.6 ms: 1.36x slower                                                                                                   |
| genshi_text                | 21.0 ms                                                                                                           | 28.7 ms: 1.36x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.12 ms                                                                                                           | 5.70 ms: 1.38x slower                                                                                                   |
| mako                       | 11.6 ms                                                                                                           | 16.3 ms: 1.40x slower                                                                                                   |
| richards                   | 41.7 ms                                                                                                           | 58.8 ms: 1.41x slower                                                                                                   |
| richards_super             | 48.2 ms                                                                                                           | 68.0 ms: 1.41x slower                                                                                                   |
| deltablue                  | 3.08 ms                                                                                                           | 4.79 ms: 1.56x slower                                                                                                   |
| nbody                      | 88.0 ms                                                                                                           | 141 ms: 1.60x slower                                                                                                    |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.34 ms: 3.24x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_io, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: html5lib

- Geometric mean (including insignificant results): 1.157x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x