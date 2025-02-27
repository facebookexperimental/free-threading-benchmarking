# Results vs. base

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.101x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 434 ms                                                                                                            | 500 ms: 1.15x slower                                                                                                    |
| docutils       | 3.68 sec                                                                                                          | 4.08 sec: 1.11x slower                                                                                                  |
| html5lib       | 84.0 ms                                                                                                           | 94.3 ms: 1.12x slower                                                                                                   |
| sphinx         | 1.42 sec                                                                                                          | 1.56 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg         | 434 ms                                                                                                            | 332 ms: 1.31x faster                                                                                                    |
| async_tree_io_tg           | 887 ms                                                                                                            | 745 ms: 1.19x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 680 ms                                                                                                            | 639 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 842 ms                                                                                                            | 805 ms: 1.04x faster                                                                                                    |
| coroutines                 | 30.8 ms                                                                                                           | 32.5 ms: 1.05x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 687 ms                                                                                                            | 734 ms: 1.07x slower                                                                                                    |
| async_tree_memoization     | 476 ms                                                                                                            | 525 ms: 1.10x slower                                                                                                    |
| asyncio_websockets         | 725 ms                                                                                                            | 805 ms: 1.11x slower                                                                                                    |
| async_generators           | 504 ms                                                                                                            | 570 ms: 1.13x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 229 ms                                                                                                            | 233 ms: 1.02x slower                                                                                                    |
| float          | 98.7 ms                                                                                                           | 105 ms: 1.06x slower                                                                                                    |
| nbody          | 121 ms                                                                                                            | 171 ms: 1.41x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 31.4 ms                                                                                                           | 33.3 ms: 1.06x slower                                                                                                   |
| regex_compile  | 160 ms                                                                                                            | 189 ms: 1.18x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|---------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse | 157 ms                                                                                                            | 134 ms: 1.18x faster                                                                                                    |
| xml_etree_parse     | 222 ms                                                                                                            | 201 ms: 1.10x faster                                                                                                    |
| xml_etree_process   | 82.8 ms                                                                                                           | 87.9 ms: 1.06x slower                                                                                                   |
| xml_etree_generate  | 116 ms                                                                                                            | 125 ms: 1.08x slower                                                                                                    |
| json_loads          | 37.3 us                                                                                                           | 42.0 us: 1.13x slower                                                                                                   |
| pickle_pure_python  | 425 us                                                                                                            | 490 us: 1.15x slower                                                                                                    |
| json_dumps          | 15.1 ms                                                                                                           | 17.6 ms: 1.17x slower                                                                                                   |
| tomli_loads         | 2.57 sec                                                                                                          | 3.01 sec: 1.17x slower                                                                                                  |
| Geometric mean      | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 27.4 ms                                                                                                           | 30.5 ms: 1.11x slower                                                                                                   |
| python_startup_no_site | 15.8 ms                                                                                                           | 19.9 ms: 1.26x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 48.4 ms                                                                                                           | 50.8 ms: 1.05x slower                                                                                                   |
| genshi_xml      | 67.7 ms                                                                                                           | 80.1 ms: 1.18x slower                                                                                                   |
| genshi_text     | 27.2 ms                                                                                                           | 35.6 ms: 1.31x slower                                                                                                   |
| mako            | 15.0 ms                                                                                                           | 22.1 ms: 1.47x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.24x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 8.25 ms                                                                                                           | 3.62 ms: 2.28x faster                                                                                                   |
| create_gc_cycles           | 4.00 ms                                                                                                           | 2.61 ms: 1.53x faster                                                                                                   |
| async_tree_none_tg         | 434 ms                                                                                                            | 332 ms: 1.31x faster                                                                                                    |
| async_tree_io_tg           | 887 ms                                                                                                            | 745 ms: 1.19x faster                                                                                                    |
| xml_etree_iterparse        | 157 ms                                                                                                            | 134 ms: 1.18x faster                                                                                                    |
| bench_mp_pool              | 94.4 ms                                                                                                           | 81.5 ms: 1.16x faster                                                                                                   |
| xml_etree_parse            | 222 ms                                                                                                            | 201 ms: 1.10x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 680 ms                                                                                                            | 639 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 842 ms                                                                                                            | 805 ms: 1.04x faster                                                                                                    |
| pidigits                   | 229 ms                                                                                                            | 233 ms: 1.02x slower                                                                                                    |
| pycparser                  | 1.47 sec                                                                                                          | 1.52 sec: 1.03x slower                                                                                                  |
| django_template            | 48.4 ms                                                                                                           | 50.8 ms: 1.05x slower                                                                                                   |
| coroutines                 | 30.8 ms                                                                                                           | 32.5 ms: 1.05x slower                                                                                                   |
| k_core                     | 3.99 sec                                                                                                          | 4.21 sec: 1.06x slower                                                                                                  |
| xml_etree_process          | 82.8 ms                                                                                                           | 87.9 ms: 1.06x slower                                                                                                   |
| regex_v8                   | 31.4 ms                                                                                                           | 33.3 ms: 1.06x slower                                                                                                   |
| float                      | 98.7 ms                                                                                                           | 105 ms: 1.06x slower                                                                                                    |
| logging_simple             | 8.22 us                                                                                                           | 8.74 us: 1.06x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 687 ms                                                                                                            | 734 ms: 1.07x slower                                                                                                    |
| logging_silent             | 136 ns                                                                                                            | 146 ns: 1.08x slower                                                                                                    |
| xml_etree_generate         | 116 ms                                                                                                            | 125 ms: 1.08x slower                                                                                                    |
| generators                 | 39.6 ms                                                                                                           | 43.1 ms: 1.09x slower                                                                                                   |
| scimark_lu                 | 168 ms                                                                                                            | 183 ms: 1.09x slower                                                                                                    |
| telco                      | 11.0 ms                                                                                                           | 12.1 ms: 1.10x slower                                                                                                   |
| sqlglot_optimize           | 71.2 ms                                                                                                           | 78.1 ms: 1.10x slower                                                                                                   |
| sphinx                     | 1.42 sec                                                                                                          | 1.56 sec: 1.10x slower                                                                                                  |
| mdp                        | 3.64 sec                                                                                                          | 4.01 sec: 1.10x slower                                                                                                  |
| async_tree_memoization     | 476 ms                                                                                                            | 525 ms: 1.10x slower                                                                                                    |
| docutils                   | 3.68 sec                                                                                                          | 4.08 sec: 1.11x slower                                                                                                  |
| asyncio_websockets         | 725 ms                                                                                                            | 805 ms: 1.11x slower                                                                                                    |
| python_startup             | 27.4 ms                                                                                                           | 30.5 ms: 1.11x slower                                                                                                   |
| shortest_path              | 919 ms                                                                                                            | 1.03 sec: 1.12x slower                                                                                                  |
| sympy_expand               | 603 ms                                                                                                            | 677 ms: 1.12x slower                                                                                                    |
| html5lib                   | 84.0 ms                                                                                                           | 94.3 ms: 1.12x slower                                                                                                   |
| json_loads                 | 37.3 us                                                                                                           | 42.0 us: 1.13x slower                                                                                                   |
| bench_thread_pool          | 3.20 ms                                                                                                           | 3.61 ms: 1.13x slower                                                                                                   |
| async_generators           | 504 ms                                                                                                            | 570 ms: 1.13x slower                                                                                                    |
| thrift                     | 998 us                                                                                                            | 1.13 ms: 1.14x slower                                                                                                   |
| pprint_safe_repr           | 952 ms                                                                                                            | 1.09 sec: 1.14x slower                                                                                                  |
| scimark_sor                | 160 ms                                                                                                            | 184 ms: 1.15x slower                                                                                                    |
| pylint                     | 389 ms                                                                                                            | 447 ms: 1.15x slower                                                                                                    |
| 2to3                       | 434 ms                                                                                                            | 500 ms: 1.15x slower                                                                                                    |
| pickle_pure_python         | 425 us                                                                                                            | 490 us: 1.15x slower                                                                                                    |
| comprehensions             | 22.1 us                                                                                                           | 25.6 us: 1.15x slower                                                                                                   |
| json_dumps                 | 15.1 ms                                                                                                           | 17.6 ms: 1.17x slower                                                                                                   |
| chaos                      | 78.9 ms                                                                                                           | 92.1 ms: 1.17x slower                                                                                                   |
| sqlalchemy_declarative     | 175 ms                                                                                                            | 205 ms: 1.17x slower                                                                                                    |
| spectral_norm              | 127 ms                                                                                                            | 148 ms: 1.17x slower                                                                                                    |
| tomli_loads                | 2.57 sec                                                                                                          | 3.01 sec: 1.17x slower                                                                                                  |
| sqlglot_transpile          | 2.22 ms                                                                                                           | 2.60 ms: 1.17x slower                                                                                                   |
| logging_format             | 9.79 us                                                                                                           | 11.5 us: 1.18x slower                                                                                                   |
| regex_compile              | 160 ms                                                                                                            | 189 ms: 1.18x slower                                                                                                    |
| genshi_xml                 | 67.7 ms                                                                                                           | 80.1 ms: 1.18x slower                                                                                                   |
| bpe_tokeniser              | 5.93 sec                                                                                                          | 7.06 sec: 1.19x slower                                                                                                  |
| connected_components       | 756 ms                                                                                                            | 901 ms: 1.19x slower                                                                                                    |
| deepcopy_reduce            | 3.57 us                                                                                                           | 4.25 us: 1.19x slower                                                                                                   |
| deltablue                  | 4.20 ms                                                                                                           | 5.02 ms: 1.20x slower                                                                                                   |
| sympy_integrate            | 27.5 ms                                                                                                           | 33.1 ms: 1.20x slower                                                                                                   |
| raytrace                   | 347 ms                                                                                                            | 420 ms: 1.21x slower                                                                                                    |
| coverage                   | 114 ms                                                                                                            | 138 ms: 1.21x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.25 ms                                                                                                           | 7.58 ms: 1.21x slower                                                                                                   |
| richards                   | 57.7 ms                                                                                                           | 70.0 ms: 1.21x slower                                                                                                   |
| sqlglot_normalize          | 132 ms                                                                                                            | 161 ms: 1.21x slower                                                                                                    |
| pprint_pformat             | 1.87 sec                                                                                                          | 2.28 sec: 1.22x slower                                                                                                  |
| sqlglot_parse              | 1.77 ms                                                                                                           | 2.16 ms: 1.22x slower                                                                                                   |
| sympy_str                  | 349 ms                                                                                                            | 429 ms: 1.23x slower                                                                                                    |
| typing_runtime_protocols   | 213 us                                                                                                            | 263 us: 1.24x slower                                                                                                    |
| pyflate                    | 616 ms                                                                                                            | 762 ms: 1.24x slower                                                                                                    |
| richards_super             | 66.6 ms                                                                                                           | 82.5 ms: 1.24x slower                                                                                                   |
| subparsers                 | 29.4 ms                                                                                                           | 36.7 ms: 1.25x slower                                                                                                   |
| hexiom                     | 8.32 ms                                                                                                           | 10.4 ms: 1.25x slower                                                                                                   |
| go                         | 145 ms                                                                                                            | 183 ms: 1.26x slower                                                                                                    |
| python_startup_no_site     | 15.8 ms                                                                                                           | 19.9 ms: 1.26x slower                                                                                                   |
| deepcopy                   | 329 us                                                                                                            | 415 us: 1.26x slower                                                                                                    |
| deepcopy_memo              | 36.8 us                                                                                                           | 47.0 us: 1.28x slower                                                                                                   |
| nqueens                    | 106 ms                                                                                                            | 136 ms: 1.28x slower                                                                                                    |
| sympy_sum                  | 198 ms                                                                                                            | 254 ms: 1.28x slower                                                                                                    |
| crypto_pyaes               | 97.3 ms                                                                                                           | 125 ms: 1.29x slower                                                                                                    |
| scimark_fft                | 418 ms                                                                                                            | 540 ms: 1.29x slower                                                                                                    |
| meteor_contest             | 135 ms                                                                                                            | 175 ms: 1.29x slower                                                                                                    |
| sqlalchemy_imperative      | 20.8 ms                                                                                                           | 27.0 ms: 1.30x slower                                                                                                   |
| many_optionals             | 1.19 ms                                                                                                           | 1.55 ms: 1.30x slower                                                                                                   |
| fannkuch                   | 509 ms                                                                                                            | 664 ms: 1.30x slower                                                                                                    |
| genshi_text                | 27.2 ms                                                                                                           | 35.6 ms: 1.31x slower                                                                                                   |
| scimark_monte_carlo        | 83.2 ms                                                                                                           | 110 ms: 1.32x slower                                                                                                    |
| nbody                      | 121 ms                                                                                                            | 171 ms: 1.41x slower                                                                                                    |
| mako                       | 15.0 ms                                                                                                           | 22.1 ms: 1.47x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (9): json, pathlib, sqlite_synth, async_tree_memoization_tg, dulwich_log, regex_dna, regex_effbot, async_tree_none, unpickle_pure_python

- Geometric mean (including insignificant results): 1.101x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x