# Results vs. base

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.129x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                                                            | 301 ms: 1.19x slower                                                                                                    |
| docutils       | 2.56 sec                                                                                                          | 2.79 sec: 1.09x slower                                                                                                  |
| sphinx         | 974 ms                                                                                                            | 1.10 sec: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 626 ms                                                                                                            | 571 ms: 1.10x faster                                                                                                    |
| async_tree_io              | 619 ms                                                                                                            | 605 ms: 1.02x faster                                                                                                    |
| coroutines                 | 22.6 ms                                                                                                           | 23.3 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                                                            | 504 ms: 1.03x slower                                                                                                    |
| async_tree_none            | 269 ms                                                                                                            | 286 ms: 1.06x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 498 ms                                                                                                            | 537 ms: 1.08x slower                                                                                                    |
| async_tree_memoization     | 321 ms                                                                                                            | 349 ms: 1.09x slower                                                                                                    |
| async_generators           | 322 ms                                                                                                            | 385 ms: 1.20x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                                                            | 191 ms: 1.02x slower                                                                                                    |
| float          | 71.6 ms                                                                                                           | 75.8 ms: 1.06x slower                                                                                                   |
| nbody          | 95.8 ms                                                                                                           | 130 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 164 ms                                                                                                            | 177 ms: 1.08x slower                                                                                                    |
| regex_compile  | 127 ms                                                                                                            | 150 ms: 1.18x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.8 ms                                                                                                           | 87.9 ms: 1.03x faster                                                                                                   |
| json_loads           | 28.4 us                                                                                                           | 31.3 us: 1.10x slower                                                                                                   |
| json_dumps           | 11.4 ms                                                                                                           | 12.8 ms: 1.12x slower                                                                                                   |
| unpickle_pure_python | 212 us                                                                                                            | 245 us: 1.15x slower                                                                                                    |
| xml_etree_generate   | 83.4 ms                                                                                                           | 96.6 ms: 1.16x slower                                                                                                   |
| xml_etree_process    | 58.1 ms                                                                                                           | 69.0 ms: 1.19x slower                                                                                                   |
| pickle_pure_python   | 308 us                                                                                                            | 366 us: 1.19x slower                                                                                                    |
| tomli_loads          | 1.88 sec                                                                                                          | 2.32 sec: 1.24x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                                                           | 15.2 ms: 1.03x slower                                                                                                   |
| python_startup_no_site | 7.51 ms                                                                                                           | 9.55 ms: 1.27x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.6 ms                                                                                                           | 59.2 ms: 1.22x slower                                                                                                   |
| django_template | 34.5 ms                                                                                                           | 42.5 ms: 1.23x slower                                                                                                   |
| genshi_text     | 20.8 ms                                                                                                           | 28.0 ms: 1.35x slower                                                                                                   |
| mako            | 11.7 ms                                                                                                           | 16.0 ms: 1.37x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.29x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json | results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.24 ms                                                                                                           | 1.73 ms: 2.45x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.38 ms: 1.35x faster                                                                                                   |
| async_tree_io_tg           | 626 ms                                                                                                            | 571 ms: 1.10x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.05 us: 1.06x faster                                                                                                   |
| xml_etree_iterparse        | 90.8 ms                                                                                                           | 87.9 ms: 1.03x faster                                                                                                   |
| async_tree_io              | 619 ms                                                                                                            | 605 ms: 1.02x faster                                                                                                    |
| pathlib                    | 18.8 ms                                                                                                           | 19.0 ms: 1.01x slower                                                                                                   |
| pidigits                   | 186 ms                                                                                                            | 191 ms: 1.02x slower                                                                                                    |
| coroutines                 | 22.6 ms                                                                                                           | 23.3 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                                                            | 504 ms: 1.03x slower                                                                                                    |
| python_startup             | 14.8 ms                                                                                                           | 15.2 ms: 1.03x slower                                                                                                   |
| pycparser                  | 1.12 sec                                                                                                          | 1.18 sec: 1.05x slower                                                                                                  |
| bench_mp_pool              | 89.2 ms                                                                                                           | 94.3 ms: 1.06x slower                                                                                                   |
| float                      | 71.6 ms                                                                                                           | 75.8 ms: 1.06x slower                                                                                                   |
| async_tree_none            | 269 ms                                                                                                            | 286 ms: 1.06x slower                                                                                                    |
| json                       | 5.06 ms                                                                                                           | 5.38 ms: 1.06x slower                                                                                                   |
| regex_dna                  | 164 ms                                                                                                            | 177 ms: 1.08x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 498 ms                                                                                                            | 537 ms: 1.08x slower                                                                                                    |
| dulwich_log                | 75.6 ms                                                                                                           | 81.8 ms: 1.08x slower                                                                                                   |
| generators                 | 29.1 ms                                                                                                           | 31.6 ms: 1.09x slower                                                                                                   |
| async_tree_memoization     | 321 ms                                                                                                            | 349 ms: 1.09x slower                                                                                                    |
| docutils                   | 2.56 sec                                                                                                          | 2.79 sec: 1.09x slower                                                                                                  |
| logging_silent             | 103 ns                                                                                                            | 113 ns: 1.10x slower                                                                                                    |
| json_loads                 | 28.4 us                                                                                                           | 31.3 us: 1.10x slower                                                                                                   |
| json_dumps                 | 11.4 ms                                                                                                           | 12.8 ms: 1.12x slower                                                                                                   |
| k_core                     | 2.05 sec                                                                                                          | 2.30 sec: 1.12x slower                                                                                                  |
| sphinx                     | 974 ms                                                                                                            | 1.10 sec: 1.13x slower                                                                                                  |
| bpe_tokeniser              | 4.13 sec                                                                                                          | 4.67 sec: 1.13x slower                                                                                                  |
| pylint                     | 278 ms                                                                                                            | 316 ms: 1.14x slower                                                                                                    |
| many_optionals             | 1.03 ms                                                                                                           | 1.17 ms: 1.14x slower                                                                                                   |
| subparsers                 | 22.1 ms                                                                                                           | 25.4 ms: 1.15x slower                                                                                                   |
| mdp                        | 2.30 sec                                                                                                          | 2.65 sec: 1.15x slower                                                                                                  |
| unpickle_pure_python       | 212 us                                                                                                            | 245 us: 1.15x slower                                                                                                    |
| xml_etree_generate         | 83.4 ms                                                                                                           | 96.6 ms: 1.16x slower                                                                                                   |
| sqlglot_normalize          | 101 ms                                                                                                            | 119 ms: 1.17x slower                                                                                                    |
| pprint_safe_repr           | 687 ms                                                                                                            | 808 ms: 1.18x slower                                                                                                    |
| pyflate                    | 415 ms                                                                                                            | 491 ms: 1.18x slower                                                                                                    |
| regex_compile              | 127 ms                                                                                                            | 150 ms: 1.18x slower                                                                                                    |
| xml_etree_process          | 58.1 ms                                                                                                           | 69.0 ms: 1.19x slower                                                                                                   |
| pickle_pure_python         | 308 us                                                                                                            | 366 us: 1.19x slower                                                                                                    |
| scimark_sor                | 113 ms                                                                                                            | 134 ms: 1.19x slower                                                                                                    |
| 2to3                       | 253 ms                                                                                                            | 301 ms: 1.19x slower                                                                                                    |
| pprint_pformat             | 1.41 sec                                                                                                          | 1.67 sec: 1.19x slower                                                                                                  |
| sqlglot_optimize           | 51.1 ms                                                                                                           | 61.0 ms: 1.19x slower                                                                                                   |
| async_generators           | 322 ms                                                                                                            | 385 ms: 1.20x slower                                                                                                    |
| spectral_norm              | 91.4 ms                                                                                                           | 109 ms: 1.20x slower                                                                                                    |
| chaos                      | 57.1 ms                                                                                                           | 68.8 ms: 1.20x slower                                                                                                   |
| telco                      | 7.16 ms                                                                                                           | 8.62 ms: 1.20x slower                                                                                                   |
| nqueens                    | 79.6 ms                                                                                                           | 96.1 ms: 1.21x slower                                                                                                   |
| go                         | 115 ms                                                                                                            | 139 ms: 1.21x slower                                                                                                    |
| sympy_expand               | 450 ms                                                                                                            | 544 ms: 1.21x slower                                                                                                    |
| deepcopy                   | 253 us                                                                                                            | 306 us: 1.21x slower                                                                                                    |
| sympy_sum                  | 151 ms                                                                                                            | 184 ms: 1.22x slower                                                                                                    |
| sqlglot_transpile          | 1.54 ms                                                                                                           | 1.88 ms: 1.22x slower                                                                                                   |
| genshi_xml                 | 48.6 ms                                                                                                           | 59.2 ms: 1.22x slower                                                                                                   |
| comprehensions             | 16.4 us                                                                                                           | 20.1 us: 1.22x slower                                                                                                   |
| thrift                     | 735 us                                                                                                            | 899 us: 1.22x slower                                                                                                    |
| sympy_integrate            | 19.5 ms                                                                                                           | 23.9 ms: 1.22x slower                                                                                                   |
| logging_simple             | 5.96 us                                                                                                           | 7.30 us: 1.23x slower                                                                                                   |
| sqlalchemy_declarative     | 127 ms                                                                                                            | 156 ms: 1.23x slower                                                                                                    |
| coverage                   | 79.0 ms                                                                                                           | 97.1 ms: 1.23x slower                                                                                                   |
| deepcopy_reduce            | 2.55 us                                                                                                           | 3.14 us: 1.23x slower                                                                                                   |
| django_template            | 34.5 ms                                                                                                           | 42.5 ms: 1.23x slower                                                                                                   |
| scimark_lu                 | 112 ms                                                                                                            | 138 ms: 1.24x slower                                                                                                    |
| tomli_loads                | 1.88 sec                                                                                                          | 2.32 sec: 1.24x slower                                                                                                  |
| logging_format             | 6.65 us                                                                                                           | 8.27 us: 1.24x slower                                                                                                   |
| sympy_str                  | 267 ms                                                                                                            | 333 ms: 1.25x slower                                                                                                    |
| raytrace                   | 262 ms                                                                                                            | 326 ms: 1.25x slower                                                                                                    |
| scimark_fft                | 310 ms                                                                                                            | 388 ms: 1.25x slower                                                                                                    |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.56 ms: 1.25x slower                                                                                                   |
| deepcopy_memo              | 30.0 us                                                                                                           | 37.7 us: 1.25x slower                                                                                                   |
| sqlalchemy_imperative      | 19.2 ms                                                                                                           | 24.1 ms: 1.26x slower                                                                                                   |
| shortest_path              | 428 ms                                                                                                            | 542 ms: 1.26x slower                                                                                                    |
| connected_components       | 390 ms                                                                                                            | 494 ms: 1.27x slower                                                                                                    |
| hexiom                     | 5.83 ms                                                                                                           | 7.40 ms: 1.27x slower                                                                                                   |
| python_startup_no_site     | 7.51 ms                                                                                                           | 9.55 ms: 1.27x slower                                                                                                   |
| scimark_monte_carlo        | 63.9 ms                                                                                                           | 82.4 ms: 1.29x slower                                                                                                   |
| meteor_contest             | 99.1 ms                                                                                                           | 129 ms: 1.30x slower                                                                                                    |
| typing_runtime_protocols   | 152 us                                                                                                            | 200 us: 1.32x slower                                                                                                    |
| crypto_pyaes               | 65.6 ms                                                                                                           | 87.2 ms: 1.33x slower                                                                                                   |
| fannkuch                   | 368 ms                                                                                                            | 490 ms: 1.33x slower                                                                                                    |
| richards                   | 42.1 ms                                                                                                           | 56.5 ms: 1.34x slower                                                                                                   |
| genshi_text                | 20.8 ms                                                                                                           | 28.0 ms: 1.35x slower                                                                                                   |
| richards_super             | 48.0 ms                                                                                                           | 65.1 ms: 1.36x slower                                                                                                   |
| nbody                      | 95.8 ms                                                                                                           | 130 ms: 1.36x slower                                                                                                    |
| mako                       | 11.7 ms                                                                                                           | 16.0 ms: 1.37x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.14 ms                                                                                                           | 5.80 ms: 1.40x slower                                                                                                   |
| deltablue                  | 3.13 ms                                                                                                           | 4.70 ms: 1.50x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.32 ms: 3.24x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (6): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg, regex_v8, xml_etree_parse, regex_effbot
Ignored benchmarks (1) of results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: html5lib

- Geometric mean (including insignificant results): 1.129x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x