# Results vs. base

- fork: python
- ref: bd2c7e8c8b10f4d31eab
- machine: linux-x86_64
- commit hash: bd2c7e8
- commit date: 2025-10-22
- overall geometric mean: 1.088x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                                                            | 281 ms: 1.13x slower                                                                                                    |
| docutils       | 2.58 sec                                                                                                          | 2.72 sec: 1.05x slower                                                                                                  |
| html5lib       | 61.5 ms                                                                                                           | 67.0 ms: 1.09x slower                                                                                                   |
| sphinx         | 974 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 592 ms                                                                                                            | 519 ms: 1.14x faster                                                                                                    |
| async_tree_none_tg         | 248 ms                                                                                                            | 227 ms: 1.09x faster                                                                                                    |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 287 ms: 1.08x faster                                                                                                    |
| asyncio_websockets         | 545 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                            | 482 ms: 1.02x faster                                                                                                    |
| async_tree_memoization     | 308 ms                                                                                                            | 313 ms: 1.02x slower                                                                                                    |
| coroutines                 | 24.1 ms                                                                                                           | 24.8 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 494 ms                                                                                                            | 510 ms: 1.03x slower                                                                                                    |
| async_generators           | 352 ms                                                                                                            | 366 ms: 1.04x slower                                                                                                    |
| async_tree_none            | 246 ms                                                                                                            | 258 ms: 1.05x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 70.7 ms                                                                                                           | 68.5 ms: 1.03x faster                                                                                                   |
| pidigits       | 193 ms                                                                                                            | 190 ms: 1.02x faster                                                                                                    |
| nbody          | 89.8 ms                                                                                                           | 123 ms: 1.37x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                                                                           | 20.8 ms: 1.09x faster                                                                                                   |
| regex_dna      | 177 ms                                                                                                            | 174 ms: 1.02x faster                                                                                                    |
| regex_effbot   | 2.69 ms                                                                                                           | 2.77 ms: 1.03x slower                                                                                                   |
| regex_compile  | 125 ms                                                                                                            | 143 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                    |
| xml_etree_iterparse  | 84.6 ms                                                                                                           | 88.2 ms: 1.04x slower                                                                                                   |
| tomli_loads          | 1.92 sec                                                                                                          | 2.03 sec: 1.06x slower                                                                                                  |
| pickle_pure_python   | 310 us                                                                                                            | 338 us: 1.09x slower                                                                                                    |
| unpickle_pure_python | 209 us                                                                                                            | 233 us: 1.11x slower                                                                                                    |
| json_dumps           | 9.74 ms                                                                                                           | 11.0 ms: 1.13x slower                                                                                                   |
| json_loads           | 28.1 us                                                                                                           | 31.7 us: 1.13x slower                                                                                                   |
| xml_etree_generate   | 82.8 ms                                                                                                           | 96.2 ms: 1.16x slower                                                                                                   |
| xml_etree_process    | 58.5 ms                                                                                                           | 69.2 ms: 1.18x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.24 ms                                                                                                           | 9.61 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                                                           | 40.5 ms: 1.17x slower                                                                                                   |
| genshi_xml      | 48.6 ms                                                                                                           | 58.0 ms: 1.19x slower                                                                                                   |
| genshi_text     | 20.9 ms                                                                                                           | 26.3 ms: 1.26x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 15.6 ms: 1.32x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.23x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json | results/bm-20251022-3.15.0a1+-bd2c7e8-NOGIL/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.68 ms                                                                                                           | 1.95 ms: 2.40x faster                                                                                                   |
| create_gc_cycles           | 1.93 ms                                                                                                           | 1.52 ms: 1.27x faster                                                                                                   |
| async_tree_io_tg           | 592 ms                                                                                                            | 519 ms: 1.14x faster                                                                                                    |
| sqlite_synth               | 2.28 us                                                                                                           | 2.07 us: 1.10x faster                                                                                                   |
| regex_v8                   | 22.7 ms                                                                                                           | 20.8 ms: 1.09x faster                                                                                                   |
| async_tree_none_tg         | 248 ms                                                                                                            | 227 ms: 1.09x faster                                                                                                    |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 287 ms: 1.08x faster                                                                                                    |
| asyncio_websockets         | 545 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| float                      | 70.7 ms                                                                                                           | 68.5 ms: 1.03x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                            | 482 ms: 1.02x faster                                                                                                    |
| pidigits                   | 193 ms                                                                                                            | 190 ms: 1.02x faster                                                                                                    |
| regex_dna                  | 177 ms                                                                                                            | 174 ms: 1.02x faster                                                                                                    |
| xml_etree_parse            | 130 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                    |
| pathlib                    | 17.7 ms                                                                                                           | 17.9 ms: 1.01x slower                                                                                                   |
| async_tree_memoization     | 308 ms                                                                                                            | 313 ms: 1.02x slower                                                                                                    |
| coroutines                 | 24.1 ms                                                                                                           | 24.8 ms: 1.03x slower                                                                                                   |
| regex_effbot               | 2.69 ms                                                                                                           | 2.77 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 494 ms                                                                                                            | 510 ms: 1.03x slower                                                                                                    |
| async_generators           | 352 ms                                                                                                            | 366 ms: 1.04x slower                                                                                                    |
| xml_etree_iterparse        | 84.6 ms                                                                                                           | 88.2 ms: 1.04x slower                                                                                                   |
| dulwich_log                | 68.8 ms                                                                                                           | 72.1 ms: 1.05x slower                                                                                                   |
| bpe_tokeniser              | 4.23 sec                                                                                                          | 4.44 sec: 1.05x slower                                                                                                  |
| async_tree_none            | 246 ms                                                                                                            | 258 ms: 1.05x slower                                                                                                    |
| docutils                   | 2.58 sec                                                                                                          | 2.72 sec: 1.05x slower                                                                                                  |
| pycparser                  | 1.09 sec                                                                                                          | 1.14 sec: 1.05x slower                                                                                                  |
| tomli_loads                | 1.92 sec                                                                                                          | 2.03 sec: 1.06x slower                                                                                                  |
| pylint                     | 288 ms                                                                                                            | 306 ms: 1.06x slower                                                                                                    |
| json                       | 5.06 ms                                                                                                           | 5.40 ms: 1.07x slower                                                                                                   |
| sympy_expand               | 479 ms                                                                                                            | 515 ms: 1.07x slower                                                                                                    |
| scimark_fft                | 316 ms                                                                                                            | 342 ms: 1.08x slower                                                                                                    |
| logging_silent             | 97.6 ns                                                                                                           | 106 ns: 1.09x slower                                                                                                    |
| telco                      | 159 ms                                                                                                            | 173 ms: 1.09x slower                                                                                                    |
| html5lib                   | 61.5 ms                                                                                                           | 67.0 ms: 1.09x slower                                                                                                   |
| pickle_pure_python         | 310 us                                                                                                            | 338 us: 1.09x slower                                                                                                    |
| generators                 | 27.7 ms                                                                                                           | 30.3 ms: 1.09x slower                                                                                                   |
| many_optionals             | 1.24 ms                                                                                                           | 1.36 ms: 1.10x slower                                                                                                   |
| sphinx                     | 974 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| deltablue                  | 3.31 ms                                                                                                           | 3.65 ms: 1.10x slower                                                                                                   |
| pprint_safe_repr           | 700 ms                                                                                                            | 777 ms: 1.11x slower                                                                                                    |
| chaos                      | 56.6 ms                                                                                                           | 63.1 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python       | 209 us                                                                                                            | 233 us: 1.11x slower                                                                                                    |
| pyflate                    | 417 ms                                                                                                            | 466 ms: 1.12x slower                                                                                                    |
| sympy_str                  | 278 ms                                                                                                            | 311 ms: 1.12x slower                                                                                                    |
| nqueens                    | 79.0 ms                                                                                                           | 88.5 ms: 1.12x slower                                                                                                   |
| sympy_sum                  | 157 ms                                                                                                            | 177 ms: 1.13x slower                                                                                                    |
| deepcopy                   | 246 us                                                                                                            | 277 us: 1.13x slower                                                                                                    |
| json_dumps                 | 9.74 ms                                                                                                           | 11.0 ms: 1.13x slower                                                                                                   |
| json_loads                 | 28.1 us                                                                                                           | 31.7 us: 1.13x slower                                                                                                   |
| pprint_pformat             | 1.42 sec                                                                                                          | 1.60 sec: 1.13x slower                                                                                                  |
| deepcopy_reduce            | 2.65 us                                                                                                           | 3.00 us: 1.13x slower                                                                                                   |
| 2to3                       | 248 ms                                                                                                            | 281 ms: 1.13x slower                                                                                                    |
| spectral_norm              | 95.8 ms                                                                                                           | 109 ms: 1.14x slower                                                                                                    |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| hexiom                     | 5.71 ms                                                                                                           | 6.50 ms: 1.14x slower                                                                                                   |
| regex_compile              | 125 ms                                                                                                            | 143 ms: 1.14x slower                                                                                                    |
| sqlglot_v2_normalize       | 101 ms                                                                                                            | 116 ms: 1.14x slower                                                                                                    |
| subparsers                 | 44.8 ms                                                                                                           | 51.3 ms: 1.14x slower                                                                                                   |
| sqlglot_v2_optimize        | 50.9 ms                                                                                                           | 58.3 ms: 1.14x slower                                                                                                   |
| sympy_integrate            | 19.1 ms                                                                                                           | 21.9 ms: 1.15x slower                                                                                                   |
| scimark_sor                | 108 ms                                                                                                            | 123 ms: 1.15x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.63 ms                                                                                                           | 5.33 ms: 1.15x slower                                                                                                   |
| thrift                     | 770 us                                                                                                            | 887 us: 1.15x slower                                                                                                    |
| logging_format             | 6.71 us                                                                                                           | 7.76 us: 1.16x slower                                                                                                   |
| logging_simple             | 5.97 us                                                                                                           | 6.92 us: 1.16x slower                                                                                                   |
| fannkuch                   | 393 ms                                                                                                            | 456 ms: 1.16x slower                                                                                                    |
| xml_etree_generate         | 82.8 ms                                                                                                           | 96.2 ms: 1.16x slower                                                                                                   |
| go                         | 104 ms                                                                                                            | 121 ms: 1.17x slower                                                                                                    |
| django_template            | 34.7 ms                                                                                                           | 40.5 ms: 1.17x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                           | 1.77 ms: 1.17x slower                                                                                                   |
| comprehensions             | 15.4 us                                                                                                           | 18.0 us: 1.17x slower                                                                                                   |
| k_core                     | 1.90 sec                                                                                                          | 2.23 sec: 1.18x slower                                                                                                  |
| raytrace                   | 253 ms                                                                                                            | 298 ms: 1.18x slower                                                                                                    |
| xml_etree_process          | 58.5 ms                                                                                                           | 69.2 ms: 1.18x slower                                                                                                   |
| deepcopy_memo              | 26.3 us                                                                                                           | 31.2 us: 1.18x slower                                                                                                   |
| meteor_contest             | 99.7 ms                                                                                                           | 119 ms: 1.19x slower                                                                                                    |
| genshi_xml                 | 48.6 ms                                                                                                           | 58.0 ms: 1.19x slower                                                                                                   |
| scimark_lu                 | 110 ms                                                                                                            | 132 ms: 1.20x slower                                                                                                    |
| typing_runtime_protocols   | 156 us                                                                                                            | 189 us: 1.21x slower                                                                                                    |
| sqlglot_v2_parse           | 1.20 ms                                                                                                           | 1.46 ms: 1.21x slower                                                                                                   |
| shortest_path              | 444 ms                                                                                                            | 539 ms: 1.21x slower                                                                                                    |
| connected_components       | 404 ms                                                                                                            | 491 ms: 1.22x slower                                                                                                    |
| crypto_pyaes               | 69.4 ms                                                                                                           | 84.7 ms: 1.22x slower                                                                                                   |
| bench_mp_pool              | 12.4 ms                                                                                                           | 15.2 ms: 1.22x slower                                                                                                   |
| scimark_monte_carlo        | 62.1 ms                                                                                                           | 78.2 ms: 1.26x slower                                                                                                   |
| richards                   | 40.9 ms                                                                                                           | 51.5 ms: 1.26x slower                                                                                                   |
| genshi_text                | 20.9 ms                                                                                                           | 26.3 ms: 1.26x slower                                                                                                   |
| richards_super             | 46.9 ms                                                                                                           | 59.3 ms: 1.26x slower                                                                                                   |
| python_startup             | 12.4 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| mako                       | 11.8 ms                                                                                                           | 15.6 ms: 1.32x slower                                                                                                   |
| python_startup_no_site     | 7.24 ms                                                                                                           | 9.61 ms: 1.33x slower                                                                                                   |
| coverage                   | 81.6 ms                                                                                                           | 111 ms: 1.36x slower                                                                                                    |
| nbody                      | 89.8 ms                                                                                                           | 123 ms: 1.37x slower                                                                                                    |
| bench_thread_pool          | 998 us                                                                                                            | 3.07 ms: 3.07x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_io

- Geometric mean (including insignificant results): 1.088x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.20x