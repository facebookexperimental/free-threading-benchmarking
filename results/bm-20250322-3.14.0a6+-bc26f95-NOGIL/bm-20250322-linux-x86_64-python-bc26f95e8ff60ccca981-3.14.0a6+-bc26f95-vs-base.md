# Results vs. base

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.124x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 404 ms                                                                                                            | 506 ms: 1.25x slower                                                                                                    |
| docutils       | 3.55 sec                                                                                                          | 3.91 sec: 1.10x slower                                                                                                  |
| sphinx         | 1.37 sec                                                                                                          | 1.63 sec: 1.20x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 877 ms                                                                                                            | 730 ms: 1.20x faster                                                                                                    |
| async_tree_none_tg         | 359 ms                                                                                                            | 331 ms: 1.08x faster                                                                                                    |
| coroutines                 | 31.8 ms                                                                                                           | 29.7 ms: 1.07x faster                                                                                                   |
| async_tree_io              | 854 ms                                                                                                            | 803 ms: 1.06x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                                                            | 633 ms: 1.05x faster                                                                                                    |
| async_tree_none            | 369 ms                                                                                                            | 384 ms: 1.04x slower                                                                                                    |
| async_tree_memoization     | 461 ms                                                                                                            | 509 ms: 1.11x slower                                                                                                    |
| asyncio_tcp_ssl            | 2.71 sec                                                                                                          | 3.21 sec: 1.18x slower                                                                                                  |
| async_generators           | 479 ms                                                                                                            | 574 ms: 1.20x slower                                                                                                    |
| asyncio_tcp                | 853 ms                                                                                                            | 1.02 sec: 1.20x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 240 ms                                                                                                            | 226 ms: 1.06x faster                                                                                                    |
| float          | 95.4 ms                                                                                                           | 101 ms: 1.06x slower                                                                                                    |
| nbody          | 129 ms                                                                                                            | 167 ms: 1.30x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 275 ms                                                                                                            | 284 ms: 1.03x slower                                                                                                    |
| regex_effbot   | 3.99 ms                                                                                                           | 4.37 ms: 1.10x slower                                                                                                   |
| regex_v8       | 30.2 ms                                                                                                           | 33.6 ms: 1.12x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_dict          | 45.6 us                                                                                                           | 43.2 us: 1.06x faster                                                                                                   |
| json_dumps           | 15.1 ms                                                                                                           | 16.5 ms: 1.09x slower                                                                                                   |
| xml_etree_parse      | 186 ms                                                                                                            | 207 ms: 1.11x slower                                                                                                    |
| json_loads           | 38.1 us                                                                                                           | 43.6 us: 1.14x slower                                                                                                   |
| unpickle_list        | 6.88 us                                                                                                           | 8.15 us: 1.18x slower                                                                                                   |
| xml_etree_generate   | 113 ms                                                                                                            | 136 ms: 1.20x slower                                                                                                    |
| unpickle_pure_python | 292 us                                                                                                            | 358 us: 1.23x slower                                                                                                    |
| xml_etree_process    | 77.6 ms                                                                                                           | 96.9 ms: 1.25x slower                                                                                                   |
| pickle_pure_python   | 399 us                                                                                                            | 506 us: 1.27x slower                                                                                                    |
| tomli_loads          | 2.43 sec                                                                                                          | 3.11 sec: 1.28x slower                                                                                                  |
| unpickle             | 18.5 us                                                                                                           | 23.9 us: 1.29x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (3): pickle, xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 17.0 ms                                                                                                           | 21.4 ms: 1.26x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 44.1 ms                                                                                                           | 52.4 ms: 1.19x slower                                                                                                   |
| genshi_xml      | 63.7 ms                                                                                                           | 76.8 ms: 1.20x slower                                                                                                   |
| genshi_text     | 27.0 ms                                                                                                           | 36.8 ms: 1.36x slower                                                                                                   |
| mako            | 16.5 ms                                                                                                           | 23.1 ms: 1.40x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.29x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.93 ms                                                                                                           | 3.51 ms: 2.26x faster                                                                                                   |
| create_gc_cycles           | 3.29 ms                                                                                                           | 2.55 ms: 1.29x faster                                                                                                   |
| async_tree_io_tg           | 877 ms                                                                                                            | 730 ms: 1.20x faster                                                                                                    |
| bench_mp_pool              | 91.4 ms                                                                                                           | 82.2 ms: 1.11x faster                                                                                                   |
| async_tree_none_tg         | 359 ms                                                                                                            | 331 ms: 1.08x faster                                                                                                    |
| coroutines                 | 31.8 ms                                                                                                           | 29.7 ms: 1.07x faster                                                                                                   |
| async_tree_io              | 854 ms                                                                                                            | 803 ms: 1.06x faster                                                                                                    |
| pidigits                   | 240 ms                                                                                                            | 226 ms: 1.06x faster                                                                                                    |
| pickle_dict                | 45.6 us                                                                                                           | 43.2 us: 1.06x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                                                            | 633 ms: 1.05x faster                                                                                                    |
| regex_dna                  | 275 ms                                                                                                            | 284 ms: 1.03x slower                                                                                                    |
| async_tree_none            | 369 ms                                                                                                            | 384 ms: 1.04x slower                                                                                                    |
| pycparser                  | 1.50 sec                                                                                                          | 1.59 sec: 1.06x slower                                                                                                  |
| dulwich_log                | 89.6 ms                                                                                                           | 95.1 ms: 1.06x slower                                                                                                   |
| float                      | 95.4 ms                                                                                                           | 101 ms: 1.06x slower                                                                                                    |
| k_core                     | 3.99 sec                                                                                                          | 4.31 sec: 1.08x slower                                                                                                  |
| pylint                     | 391 ms                                                                                                            | 428 ms: 1.09x slower                                                                                                    |
| json_dumps                 | 15.1 ms                                                                                                           | 16.5 ms: 1.09x slower                                                                                                   |
| regex_effbot               | 3.99 ms                                                                                                           | 4.37 ms: 1.10x slower                                                                                                   |
| hexiom                     | 8.50 ms                                                                                                           | 9.33 ms: 1.10x slower                                                                                                   |
| docutils                   | 3.55 sec                                                                                                          | 3.91 sec: 1.10x slower                                                                                                  |
| async_tree_memoization     | 461 ms                                                                                                            | 509 ms: 1.11x slower                                                                                                    |
| shortest_path              | 869 ms                                                                                                            | 961 ms: 1.11x slower                                                                                                    |
| json                       | 6.57 ms                                                                                                           | 7.31 ms: 1.11x slower                                                                                                   |
| xml_etree_parse            | 186 ms                                                                                                            | 207 ms: 1.11x slower                                                                                                    |
| regex_v8                   | 30.2 ms                                                                                                           | 33.6 ms: 1.12x slower                                                                                                   |
| connected_components       | 786 ms                                                                                                            | 880 ms: 1.12x slower                                                                                                    |
| chaos                      | 78.6 ms                                                                                                           | 88.0 ms: 1.12x slower                                                                                                   |
| meteor_contest             | 146 ms                                                                                                            | 164 ms: 1.12x slower                                                                                                    |
| sqlglot_v2_normalize       | 136 ms                                                                                                            | 152 ms: 1.12x slower                                                                                                    |
| scimark_sor                | 152 ms                                                                                                            | 171 ms: 1.13x slower                                                                                                    |
| sqlite_synth               | 3.52 us                                                                                                           | 3.97 us: 1.13x slower                                                                                                   |
| generators                 | 38.4 ms                                                                                                           | 43.6 ms: 1.13x slower                                                                                                   |
| mdp                        | 3.46 sec                                                                                                          | 3.92 sec: 1.14x slower                                                                                                  |
| pyflate                    | 620 ms                                                                                                            | 704 ms: 1.14x slower                                                                                                    |
| deepcopy_reduce            | 3.75 us                                                                                                           | 4.27 us: 1.14x slower                                                                                                   |
| json_loads                 | 38.1 us                                                                                                           | 43.6 us: 1.14x slower                                                                                                   |
| pprint_safe_repr           | 938 ms                                                                                                            | 1.08 sec: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.88 sec                                                                                                          | 2.16 sec: 1.15x slower                                                                                                  |
| nqueens                    | 107 ms                                                                                                            | 123 ms: 1.15x slower                                                                                                    |
| logging_simple             | 7.86 us                                                                                                           | 9.08 us: 1.16x slower                                                                                                   |
| spectral_norm              | 125 ms                                                                                                            | 147 ms: 1.17x slower                                                                                                    |
| crypto_pyaes               | 93.4 ms                                                                                                           | 110 ms: 1.18x slower                                                                                                    |
| asyncio_tcp_ssl            | 2.71 sec                                                                                                          | 3.21 sec: 1.18x slower                                                                                                  |
| unpickle_list              | 6.88 us                                                                                                           | 8.15 us: 1.18x slower                                                                                                   |
| django_template            | 44.1 ms                                                                                                           | 52.4 ms: 1.19x slower                                                                                                   |
| sympy_integrate            | 26.6 ms                                                                                                           | 31.8 ms: 1.19x slower                                                                                                   |
| bpe_tokeniser              | 5.81 sec                                                                                                          | 6.95 sec: 1.20x slower                                                                                                  |
| sphinx                     | 1.37 sec                                                                                                          | 1.63 sec: 1.20x slower                                                                                                  |
| go                         | 156 ms                                                                                                            | 187 ms: 1.20x slower                                                                                                    |
| xml_etree_generate         | 113 ms                                                                                                            | 136 ms: 1.20x slower                                                                                                    |
| async_generators           | 479 ms                                                                                                            | 574 ms: 1.20x slower                                                                                                    |
| asyncio_tcp                | 853 ms                                                                                                            | 1.02 sec: 1.20x slower                                                                                                  |
| genshi_xml                 | 63.7 ms                                                                                                           | 76.8 ms: 1.20x slower                                                                                                   |
| logging_silent             | 117 ns                                                                                                            | 141 ns: 1.20x slower                                                                                                    |
| scimark_lu                 | 150 ms                                                                                                            | 181 ms: 1.21x slower                                                                                                    |
| sympy_expand               | 575 ms                                                                                                            | 699 ms: 1.21x slower                                                                                                    |
| sqlalchemy_declarative     | 173 ms                                                                                                            | 211 ms: 1.22x slower                                                                                                    |
| deepcopy                   | 330 us                                                                                                            | 403 us: 1.22x slower                                                                                                    |
| sympy_sum                  | 198 ms                                                                                                            | 241 ms: 1.22x slower                                                                                                    |
| unpickle_pure_python       | 292 us                                                                                                            | 358 us: 1.23x slower                                                                                                    |
| many_optionals             | 1.18 ms                                                                                                           | 1.44 ms: 1.23x slower                                                                                                   |
| fannkuch                   | 529 ms                                                                                                            | 648 ms: 1.23x slower                                                                                                    |
| richards                   | 57.6 ms                                                                                                           | 71.3 ms: 1.24x slower                                                                                                   |
| unpack_sequence            | 62.7 ns                                                                                                           | 78.0 ns: 1.24x slower                                                                                                   |
| xml_etree_process          | 77.6 ms                                                                                                           | 96.9 ms: 1.25x slower                                                                                                   |
| comprehensions             | 20.9 us                                                                                                           | 26.1 us: 1.25x slower                                                                                                   |
| 2to3                       | 404 ms                                                                                                            | 506 ms: 1.25x slower                                                                                                    |
| raytrace                   | 342 ms                                                                                                            | 428 ms: 1.25x slower                                                                                                    |
| python_startup_no_site     | 17.0 ms                                                                                                           | 21.4 ms: 1.26x slower                                                                                                   |
| pickle_pure_python         | 399 us                                                                                                            | 506 us: 1.27x slower                                                                                                    |
| scimark_fft                | 438 ms                                                                                                            | 556 ms: 1.27x slower                                                                                                    |
| sqlglot_v2_optimize        | 68.6 ms                                                                                                           | 87.4 ms: 1.27x slower                                                                                                   |
| logging_format             | 8.82 us                                                                                                           | 11.3 us: 1.28x slower                                                                                                   |
| tomli_loads                | 2.43 sec                                                                                                          | 3.11 sec: 1.28x slower                                                                                                  |
| coverage                   | 122 ms                                                                                                            | 156 ms: 1.28x slower                                                                                                    |
| subparsers                 | 28.4 ms                                                                                                           | 36.6 ms: 1.29x slower                                                                                                   |
| unpickle                   | 18.5 us                                                                                                           | 23.9 us: 1.29x slower                                                                                                   |
| scimark_monte_carlo        | 86.9 ms                                                                                                           | 113 ms: 1.30x slower                                                                                                    |
| sqlglot_v2_parse           | 1.70 ms                                                                                                           | 2.21 ms: 1.30x slower                                                                                                   |
| nbody                      | 129 ms                                                                                                            | 167 ms: 1.30x slower                                                                                                    |
| richards_super             | 66.4 ms                                                                                                           | 86.6 ms: 1.30x slower                                                                                                   |
| telco                      | 10.2 ms                                                                                                           | 13.5 ms: 1.32x slower                                                                                                   |
| sqlglot_v2_transpile       | 2.22 ms                                                                                                           | 2.95 ms: 1.33x slower                                                                                                   |
| thrift                     | 965 us                                                                                                            | 1.28 ms: 1.33x slower                                                                                                   |
| sympy_str                  | 338 ms                                                                                                            | 449 ms: 1.33x slower                                                                                                    |
| deltablue                  | 4.04 ms                                                                                                           | 5.40 ms: 1.34x slower                                                                                                   |
| scimark_sparse_mat_mult    | 6.32 ms                                                                                                           | 8.47 ms: 1.34x slower                                                                                                   |
| typing_runtime_protocols   | 214 us                                                                                                            | 289 us: 1.35x slower                                                                                                    |
| genshi_text                | 27.0 ms                                                                                                           | 36.8 ms: 1.36x slower                                                                                                   |
| deepcopy_memo              | 36.3 us                                                                                                           | 49.8 us: 1.37x slower                                                                                                   |
| mako                       | 16.5 ms                                                                                                           | 23.1 ms: 1.40x slower                                                                                                   |
| sqlalchemy_imperative      | 21.9 ms                                                                                                           | 33.1 ms: 1.51x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (10): pickle, xml_etree_iterparse, asyncio_websockets, async_tree_memoization_tg, pathlib, python_startup, async_tree_cpu_io_mixed, regex_compile, bench_thread_pool, pickle_list
Ignored benchmarks (1) of results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: html5lib

- Geometric mean (including insignificant results): 1.124x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x