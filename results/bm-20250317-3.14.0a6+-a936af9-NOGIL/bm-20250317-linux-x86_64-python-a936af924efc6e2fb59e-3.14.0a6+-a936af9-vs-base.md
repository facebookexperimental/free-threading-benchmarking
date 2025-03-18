# Results vs. base

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.088x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 494 ms                                                                                                            | 540 ms: 1.09x slower                                                                                                    |
| docutils       | 3.82 sec                                                                                                          | 4.13 sec: 1.08x slower                                                                                                  |
| sphinx         | 1.45 sec                                                                                                          | 1.63 sec: 1.12x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 963 ms                                                                                                            | 733 ms: 1.31x faster                                                                                                    |
| async_tree_none_tg         | 389 ms                                                                                                            | 314 ms: 1.24x faster                                                                                                    |
| async_tree_memoization_tg  | 528 ms                                                                                                            | 454 ms: 1.16x faster                                                                                                    |
| async_tree_io              | 921 ms                                                                                                            | 812 ms: 1.13x faster                                                                                                    |
| coroutines                 | 31.6 ms                                                                                                           | 29.8 ms: 1.06x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 717 ms                                                                                                            | 681 ms: 1.05x faster                                                                                                    |
| async_tree_memoization     | 523 ms                                                                                                            | 501 ms: 1.04x faster                                                                                                    |
| async_tree_none            | 373 ms                                                                                                            | 390 ms: 1.05x slower                                                                                                    |
| async_generators           | 531 ms                                                                                                            | 590 ms: 1.11x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x faster                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 136 ms                                                                                                            | 172 ms: 1.27x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                                                                            | 304 ms: 1.09x slower                                                                                                    |
| regex_effbot   | 3.88 ms                                                                                                           | 4.25 ms: 1.09x slower                                                                                                   |
| regex_compile  | 161 ms                                                                                                            | 212 ms: 1.32x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 162 ms                                                                                                            | 140 ms: 1.16x faster                                                                                                    |
| json_dumps           | 15.5 ms                                                                                                           | 16.8 ms: 1.08x slower                                                                                                   |
| xml_etree_process    | 83.1 ms                                                                                                           | 92.3 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python | 284 us                                                                                                            | 321 us: 1.13x slower                                                                                                    |
| json_loads           | 40.2 us                                                                                                           | 47.8 us: 1.19x slower                                                                                                   |
| tomli_loads          | 2.55 sec                                                                                                          | 3.09 sec: 1.21x slower                                                                                                  |
| xml_etree_generate   | 118 ms                                                                                                            | 145 ms: 1.23x slower                                                                                                    |
| pickle_pure_python   | 421 us                                                                                                            | 523 us: 1.24x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 32.1 ms                                                                                                           | 34.9 ms: 1.09x slower                                                                                                   |
| python_startup_no_site | 19.7 ms                                                                                                           | 25.6 ms: 1.30x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 48.2 ms                                                                                                           | 55.3 ms: 1.15x slower                                                                                                   |
| genshi_xml      | 67.8 ms                                                                                                           | 87.3 ms: 1.29x slower                                                                                                   |
| mako            | 18.9 ms                                                                                                           | 25.0 ms: 1.32x slower                                                                                                   |
| genshi_text     | 28.6 ms                                                                                                           | 39.5 ms: 1.38x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.28x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 9.00 ms                                                                                                           | 3.97 ms: 2.27x faster                                                                                                   |
| create_gc_cycles           | 4.91 ms                                                                                                           | 2.72 ms: 1.80x faster                                                                                                   |
| async_tree_io_tg           | 963 ms                                                                                                            | 733 ms: 1.31x faster                                                                                                    |
| bench_mp_pool              | 109 ms                                                                                                            | 84.8 ms: 1.28x faster                                                                                                   |
| async_tree_none_tg         | 389 ms                                                                                                            | 314 ms: 1.24x faster                                                                                                    |
| async_tree_memoization_tg  | 528 ms                                                                                                            | 454 ms: 1.16x faster                                                                                                    |
| xml_etree_iterparse        | 162 ms                                                                                                            | 140 ms: 1.16x faster                                                                                                    |
| bench_thread_pool          | 4.39 ms                                                                                                           | 3.85 ms: 1.14x faster                                                                                                   |
| async_tree_io              | 921 ms                                                                                                            | 812 ms: 1.13x faster                                                                                                    |
| coroutines                 | 31.6 ms                                                                                                           | 29.8 ms: 1.06x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 717 ms                                                                                                            | 681 ms: 1.05x faster                                                                                                    |
| async_tree_memoization     | 523 ms                                                                                                            | 501 ms: 1.04x faster                                                                                                    |
| shortest_path              | 975 ms                                                                                                            | 1.02 sec: 1.04x slower                                                                                                  |
| async_tree_none            | 373 ms                                                                                                            | 390 ms: 1.05x slower                                                                                                    |
| pyflate                    | 679 ms                                                                                                            | 711 ms: 1.05x slower                                                                                                    |
| pylint                     | 428 ms                                                                                                            | 450 ms: 1.05x slower                                                                                                    |
| chaos                      | 89.1 ms                                                                                                           | 94.2 ms: 1.06x slower                                                                                                   |
| many_optionals             | 1.40 ms                                                                                                           | 1.49 ms: 1.06x slower                                                                                                   |
| dulwich_log                | 81.5 ms                                                                                                           | 87.7 ms: 1.08x slower                                                                                                   |
| sqlglot_normalize          | 144 ms                                                                                                            | 156 ms: 1.08x slower                                                                                                    |
| docutils                   | 3.82 sec                                                                                                          | 4.13 sec: 1.08x slower                                                                                                  |
| json_dumps                 | 15.5 ms                                                                                                           | 16.8 ms: 1.08x slower                                                                                                   |
| generators                 | 40.6 ms                                                                                                           | 44.2 ms: 1.09x slower                                                                                                   |
| python_startup             | 32.1 ms                                                                                                           | 34.9 ms: 1.09x slower                                                                                                   |
| regex_dna                  | 278 ms                                                                                                            | 304 ms: 1.09x slower                                                                                                    |
| regex_effbot               | 3.88 ms                                                                                                           | 4.25 ms: 1.09x slower                                                                                                   |
| 2to3                       | 494 ms                                                                                                            | 540 ms: 1.09x slower                                                                                                    |
| async_generators           | 531 ms                                                                                                            | 590 ms: 1.11x slower                                                                                                    |
| xml_etree_process          | 83.1 ms                                                                                                           | 92.3 ms: 1.11x slower                                                                                                   |
| sqlglot_optimize           | 74.0 ms                                                                                                           | 82.4 ms: 1.11x slower                                                                                                   |
| deepcopy                   | 354 us                                                                                                            | 395 us: 1.12x slower                                                                                                    |
| sphinx                     | 1.45 sec                                                                                                          | 1.63 sec: 1.12x slower                                                                                                  |
| spectral_norm              | 130 ms                                                                                                            | 147 ms: 1.13x slower                                                                                                    |
| unpickle_pure_python       | 284 us                                                                                                            | 321 us: 1.13x slower                                                                                                    |
| deltablue                  | 4.49 ms                                                                                                           | 5.08 ms: 1.13x slower                                                                                                   |
| connected_components       | 835 ms                                                                                                            | 948 ms: 1.14x slower                                                                                                    |
| logging_format             | 9.73 us                                                                                                           | 11.1 us: 1.14x slower                                                                                                   |
| mdp                        | 3.70 sec                                                                                                          | 4.22 sec: 1.14x slower                                                                                                  |
| scimark_sor                | 152 ms                                                                                                            | 174 ms: 1.14x slower                                                                                                    |
| bpe_tokeniser              | 6.46 sec                                                                                                          | 7.38 sec: 1.14x slower                                                                                                  |
| django_template            | 48.2 ms                                                                                                           | 55.3 ms: 1.15x slower                                                                                                   |
| crypto_pyaes               | 99.7 ms                                                                                                           | 114 ms: 1.15x slower                                                                                                    |
| pathlib                    | 27.3 ms                                                                                                           | 31.4 ms: 1.15x slower                                                                                                   |
| hexiom                     | 8.66 ms                                                                                                           | 9.98 ms: 1.15x slower                                                                                                   |
| meteor_contest             | 150 ms                                                                                                            | 174 ms: 1.16x slower                                                                                                    |
| sympy_integrate            | 29.3 ms                                                                                                           | 34.0 ms: 1.16x slower                                                                                                   |
| fannkuch                   | 542 ms                                                                                                            | 631 ms: 1.16x slower                                                                                                    |
| sympy_expand               | 595 ms                                                                                                            | 696 ms: 1.17x slower                                                                                                    |
| richards                   | 59.9 ms                                                                                                           | 70.1 ms: 1.17x slower                                                                                                   |
| comprehensions             | 21.9 us                                                                                                           | 25.7 us: 1.17x slower                                                                                                   |
| pprint_safe_repr           | 952 ms                                                                                                            | 1.12 sec: 1.18x slower                                                                                                  |
| coverage                   | 119 ms                                                                                                            | 141 ms: 1.18x slower                                                                                                    |
| subparsers                 | 31.6 ms                                                                                                           | 37.5 ms: 1.18x slower                                                                                                   |
| json_loads                 | 40.2 us                                                                                                           | 47.8 us: 1.19x slower                                                                                                   |
| raytrace                   | 362 ms                                                                                                            | 430 ms: 1.19x slower                                                                                                    |
| deepcopy_reduce            | 3.37 us                                                                                                           | 4.01 us: 1.19x slower                                                                                                   |
| pprint_pformat             | 1.93 sec                                                                                                          | 2.29 sec: 1.19x slower                                                                                                  |
| scimark_fft                | 445 ms                                                                                                            | 533 ms: 1.20x slower                                                                                                    |
| go                         | 162 ms                                                                                                            | 194 ms: 1.20x slower                                                                                                    |
| scimark_monte_carlo        | 88.8 ms                                                                                                           | 107 ms: 1.21x slower                                                                                                    |
| sqlglot_transpile          | 2.17 ms                                                                                                           | 2.62 ms: 1.21x slower                                                                                                   |
| tomli_loads                | 2.55 sec                                                                                                          | 3.09 sec: 1.21x slower                                                                                                  |
| thrift                     | 1.05 ms                                                                                                           | 1.27 ms: 1.21x slower                                                                                                   |
| logging_simple             | 9.02 us                                                                                                           | 11.0 us: 1.22x slower                                                                                                   |
| sympy_str                  | 351 ms                                                                                                            | 429 ms: 1.22x slower                                                                                                    |
| richards_super             | 70.4 ms                                                                                                           | 86.4 ms: 1.23x slower                                                                                                   |
| nqueens                    | 105 ms                                                                                                            | 130 ms: 1.23x slower                                                                                                    |
| xml_etree_generate         | 118 ms                                                                                                            | 145 ms: 1.23x slower                                                                                                    |
| telco                      | 9.88 ms                                                                                                           | 12.2 ms: 1.24x slower                                                                                                   |
| pickle_pure_python         | 421 us                                                                                                            | 523 us: 1.24x slower                                                                                                    |
| sqlglot_parse              | 1.84 ms                                                                                                           | 2.30 ms: 1.24x slower                                                                                                   |
| sympy_sum                  | 200 ms                                                                                                            | 251 ms: 1.26x slower                                                                                                    |
| sqlalchemy_declarative     | 181 ms                                                                                                            | 228 ms: 1.26x slower                                                                                                    |
| scimark_lu                 | 145 ms                                                                                                            | 183 ms: 1.26x slower                                                                                                    |
| nbody                      | 136 ms                                                                                                            | 172 ms: 1.27x slower                                                                                                    |
| typing_runtime_protocols   | 216 us                                                                                                            | 275 us: 1.27x slower                                                                                                    |
| deepcopy_memo              | 37.9 us                                                                                                           | 48.4 us: 1.28x slower                                                                                                   |
| genshi_xml                 | 67.8 ms                                                                                                           | 87.3 ms: 1.29x slower                                                                                                   |
| sqlalchemy_imperative      | 24.0 ms                                                                                                           | 31.2 ms: 1.30x slower                                                                                                   |
| python_startup_no_site     | 19.7 ms                                                                                                           | 25.6 ms: 1.30x slower                                                                                                   |
| scimark_sparse_mat_mult    | 6.31 ms                                                                                                           | 8.25 ms: 1.31x slower                                                                                                   |
| regex_compile              | 161 ms                                                                                                            | 212 ms: 1.32x slower                                                                                                    |
| mako                       | 18.9 ms                                                                                                           | 25.0 ms: 1.32x slower                                                                                                   |
| genshi_text                | 28.6 ms                                                                                                           | 39.5 ms: 1.38x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (11): sqlite_synth, asyncio_websockets, regex_v8, xml_etree_parse, pidigits, json, logging_silent, k_core, pycparser, async_tree_cpu_io_mixed, float
Ignored benchmarks (1) of results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: html5lib

- Geometric mean (including insignificant results): 1.088x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x