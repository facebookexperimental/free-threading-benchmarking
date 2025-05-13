# Results vs. base

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.084x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 335 ms                                                                                                          | 384 ms: 1.15x slower                                                                                                  |
| docutils       | 3.39 sec                                                                                                        | 3.62 sec: 1.07x slower                                                                                                |
| html5lib       | 76.1 ms                                                                                                         | 82.0 ms: 1.08x slower                                                                                                 |
| sphinx         | 1.30 sec                                                                                                        | 1.44 sec: 1.10x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 828 ms                                                                                                          | 677 ms: 1.22x faster                                                                                                  |
| async_tree_none_tg         | 327 ms                                                                                                          | 294 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 795 ms                                                                                                          | 727 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 619 ms                                                                                                          | 585 ms: 1.06x faster                                                                                                  |
| async_tree_memoization_tg  | 413 ms                                                                                                          | 395 ms: 1.05x faster                                                                                                  |
| coroutines                 | 28.7 ms                                                                                                         | 29.2 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 612 ms                                                                                                          | 638 ms: 1.04x slower                                                                                                  |
| asyncio_websockets         | 645 ms                                                                                                          | 674 ms: 1.04x slower                                                                                                  |
| async_generators           | 497 ms                                                                                                          | 538 ms: 1.08x slower                                                                                                  |
| async_tree_memoization     | 406 ms                                                                                                          | 440 ms: 1.08x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 232 ms                                                                                                          | 215 ms: 1.08x faster                                                                                                  |
| float          | 95.0 ms                                                                                                         | 90.3 ms: 1.05x faster                                                                                                 |
| nbody          | 117 ms                                                                                                          | 154 ms: 1.31x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 29.0 ms                                                                                                         | 26.8 ms: 1.08x faster                                                                                                 |
| regex_dna      | 253 ms                                                                                                          | 249 ms: 1.01x faster                                                                                                  |
| regex_compile  | 153 ms                                                                                                          | 178 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 125 ms                                                                                                          | 118 ms: 1.06x faster                                                                                                  |
| xml_etree_parse      | 173 ms                                                                                                          | 171 ms: 1.01x faster                                                                                                  |
| pickle_pure_python   | 391 us                                                                                                          | 427 us: 1.09x slower                                                                                                  |
| json_loads           | 37.6 us                                                                                                         | 41.2 us: 1.10x slower                                                                                                 |
| unpickle_pure_python | 270 us                                                                                                          | 298 us: 1.10x slower                                                                                                  |
| tomli_loads          | 2.49 sec                                                                                                        | 2.77 sec: 1.11x slower                                                                                                |
| json_dumps           | 14.9 ms                                                                                                         | 17.1 ms: 1.14x slower                                                                                                 |
| xml_etree_generate   | 110 ms                                                                                                          | 130 ms: 1.19x slower                                                                                                  |
| xml_etree_process    | 74.6 ms                                                                                                         | 91.1 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 17.7 ms                                                                                                         | 22.4 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 10.5 ms                                                                                                         | 13.7 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 42.5 ms                                                                                                         | 48.4 ms: 1.14x slower                                                                                                 |
| genshi_xml      | 60.7 ms                                                                                                         | 72.2 ms: 1.19x slower                                                                                                 |
| mako            | 16.2 ms                                                                                                         | 20.7 ms: 1.28x slower                                                                                                 |
| genshi_text     | 26.1 ms                                                                                                         | 33.7 ms: 1.29x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json | results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 6.41 ms                                                                                                         | 2.89 ms: 2.22x faster                                                                                                 |
| create_gc_cycles           | 3.15 ms                                                                                                         | 2.19 ms: 1.44x faster                                                                                                 |
| async_tree_io_tg           | 828 ms                                                                                                          | 677 ms: 1.22x faster                                                                                                  |
| async_tree_none_tg         | 327 ms                                                                                                          | 294 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 3.27 us                                                                                                         | 2.95 us: 1.11x faster                                                                                                 |
| bench_mp_pool              | 82.0 ms                                                                                                         | 74.3 ms: 1.10x faster                                                                                                 |
| async_tree_io              | 795 ms                                                                                                          | 727 ms: 1.09x faster                                                                                                  |
| regex_v8                   | 29.0 ms                                                                                                         | 26.8 ms: 1.08x faster                                                                                                 |
| pidigits                   | 232 ms                                                                                                          | 215 ms: 1.08x faster                                                                                                  |
| xml_etree_iterparse        | 125 ms                                                                                                          | 118 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 619 ms                                                                                                          | 585 ms: 1.06x faster                                                                                                  |
| float                      | 95.0 ms                                                                                                         | 90.3 ms: 1.05x faster                                                                                                 |
| async_tree_memoization_tg  | 413 ms                                                                                                          | 395 ms: 1.05x faster                                                                                                  |
| pycparser                  | 1.42 sec                                                                                                        | 1.39 sec: 1.02x faster                                                                                                |
| regex_dna                  | 253 ms                                                                                                          | 249 ms: 1.01x faster                                                                                                  |
| xml_etree_parse            | 173 ms                                                                                                          | 171 ms: 1.01x faster                                                                                                  |
| pathlib                    | 24.2 ms                                                                                                         | 24.0 ms: 1.01x faster                                                                                                 |
| coroutines                 | 28.7 ms                                                                                                         | 29.2 ms: 1.02x slower                                                                                                 |
| k_core                     | 3.47 sec                                                                                                        | 3.55 sec: 1.02x slower                                                                                                |
| json                       | 6.83 ms                                                                                                         | 7.06 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 612 ms                                                                                                          | 638 ms: 1.04x slower                                                                                                  |
| asyncio_websockets         | 645 ms                                                                                                          | 674 ms: 1.04x slower                                                                                                  |
| deltablue                  | 4.22 ms                                                                                                         | 4.42 ms: 1.05x slower                                                                                                 |
| spectral_norm              | 130 ms                                                                                                          | 136 ms: 1.05x slower                                                                                                  |
| generators                 | 39.6 ms                                                                                                         | 42.0 ms: 1.06x slower                                                                                                 |
| docutils                   | 3.39 sec                                                                                                        | 3.62 sec: 1.07x slower                                                                                                |
| dulwich_log                | 73.2 ms                                                                                                         | 78.1 ms: 1.07x slower                                                                                                 |
| bench_thread_pool          | 1.73 ms                                                                                                         | 1.86 ms: 1.07x slower                                                                                                 |
| scimark_sor                | 146 ms                                                                                                          | 157 ms: 1.08x slower                                                                                                  |
| html5lib                   | 76.1 ms                                                                                                         | 82.0 ms: 1.08x slower                                                                                                 |
| async_generators           | 497 ms                                                                                                          | 538 ms: 1.08x slower                                                                                                  |
| scimark_fft                | 443 ms                                                                                                          | 480 ms: 1.08x slower                                                                                                  |
| async_tree_memoization     | 406 ms                                                                                                          | 440 ms: 1.08x slower                                                                                                  |
| pylint                     | 366 ms                                                                                                          | 400 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 391 us                                                                                                          | 427 us: 1.09x slower                                                                                                  |
| json_loads                 | 37.6 us                                                                                                         | 41.2 us: 1.10x slower                                                                                                 |
| pyflate                    | 588 ms                                                                                                          | 645 ms: 1.10x slower                                                                                                  |
| chaos                      | 73.6 ms                                                                                                         | 80.8 ms: 1.10x slower                                                                                                 |
| unpickle_pure_python       | 270 us                                                                                                          | 298 us: 1.10x slower                                                                                                  |
| sphinx                     | 1.30 sec                                                                                                        | 1.44 sec: 1.10x slower                                                                                                |
| pprint_safe_repr           | 906 ms                                                                                                          | 1.00 sec: 1.10x slower                                                                                                |
| tomli_loads                | 2.49 sec                                                                                                        | 2.77 sec: 1.11x slower                                                                                                |
| bpe_tokeniser              | 5.45 sec                                                                                                        | 6.07 sec: 1.11x slower                                                                                                |
| sqlglot_v2_normalize       | 129 ms                                                                                                          | 144 ms: 1.12x slower                                                                                                  |
| scimark_lu                 | 146 ms                                                                                                          | 163 ms: 1.12x slower                                                                                                  |
| many_optionals             | 1.18 ms                                                                                                         | 1.32 ms: 1.12x slower                                                                                                 |
| pprint_pformat             | 1.84 sec                                                                                                        | 2.07 sec: 1.13x slower                                                                                                |
| nqueens                    | 98.3 ms                                                                                                         | 111 ms: 1.13x slower                                                                                                  |
| telco                      | 9.34 ms                                                                                                         | 10.5 ms: 1.13x slower                                                                                                 |
| raytrace                   | 337 ms                                                                                                          | 383 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_optimize        | 65.0 ms                                                                                                         | 73.9 ms: 1.14x slower                                                                                                 |
| deepcopy_reduce            | 3.35 us                                                                                                         | 3.81 us: 1.14x slower                                                                                                 |
| django_template            | 42.5 ms                                                                                                         | 48.4 ms: 1.14x slower                                                                                                 |
| json_dumps                 | 14.9 ms                                                                                                         | 17.1 ms: 1.14x slower                                                                                                 |
| go                         | 140 ms                                                                                                          | 161 ms: 1.15x slower                                                                                                  |
| 2to3                       | 335 ms                                                                                                          | 384 ms: 1.15x slower                                                                                                  |
| logging_silent             | 606 ns                                                                                                          | 697 ns: 1.15x slower                                                                                                  |
| deepcopy                   | 321 us                                                                                                          | 369 us: 1.15x slower                                                                                                  |
| logging_format             | 8.96 us                                                                                                         | 10.4 us: 1.16x slower                                                                                                 |
| connected_components       | 664 ms                                                                                                          | 773 ms: 1.16x slower                                                                                                  |
| regex_compile              | 153 ms                                                                                                          | 178 ms: 1.17x slower                                                                                                  |
| logging_simple             | 8.23 us                                                                                                         | 9.59 us: 1.17x slower                                                                                                 |
| thrift                     | 941 us                                                                                                          | 1.10 ms: 1.17x slower                                                                                                 |
| sympy_expand               | 551 ms                                                                                                          | 644 ms: 1.17x slower                                                                                                  |
| subparsers                 | 29.8 ms                                                                                                         | 34.8 ms: 1.17x slower                                                                                                 |
| shortest_path              | 740 ms                                                                                                          | 867 ms: 1.17x slower                                                                                                  |
| sympy_sum                  | 186 ms                                                                                                          | 218 ms: 1.17x slower                                                                                                  |
| comprehensions             | 21.2 us                                                                                                         | 24.9 us: 1.18x slower                                                                                                 |
| hexiom                     | 7.47 ms                                                                                                         | 8.78 ms: 1.18x slower                                                                                                 |
| scimark_sparse_mat_mult    | 6.02 ms                                                                                                         | 7.08 ms: 1.18x slower                                                                                                 |
| xml_etree_generate         | 110 ms                                                                                                          | 130 ms: 1.19x slower                                                                                                  |
| sympy_str                  | 325 ms                                                                                                          | 387 ms: 1.19x slower                                                                                                  |
| genshi_xml                 | 60.7 ms                                                                                                         | 72.2 ms: 1.19x slower                                                                                                 |
| scimark_monte_carlo        | 81.8 ms                                                                                                         | 97.5 ms: 1.19x slower                                                                                                 |
| fannkuch                   | 501 ms                                                                                                          | 604 ms: 1.20x slower                                                                                                  |
| sympy_integrate            | 23.6 ms                                                                                                         | 28.5 ms: 1.21x slower                                                                                                 |
| crypto_pyaes               | 91.7 ms                                                                                                         | 111 ms: 1.21x slower                                                                                                  |
| richards                   | 53.4 ms                                                                                                         | 64.6 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.93 ms                                                                                                         | 2.34 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.55 ms                                                                                                         | 1.88 ms: 1.21x slower                                                                                                 |
| richards_super             | 61.2 ms                                                                                                         | 74.6 ms: 1.22x slower                                                                                                 |
| xml_etree_process          | 74.6 ms                                                                                                         | 91.1 ms: 1.22x slower                                                                                                 |
| mdp                        | 1.68 sec                                                                                                        | 2.06 sec: 1.23x slower                                                                                                |
| meteor_contest             | 128 ms                                                                                                          | 157 ms: 1.23x slower                                                                                                  |
| deepcopy_memo              | 36.5 us                                                                                                         | 45.2 us: 1.24x slower                                                                                                 |
| python_startup             | 17.7 ms                                                                                                         | 22.4 ms: 1.26x slower                                                                                                 |
| mako                       | 16.2 ms                                                                                                         | 20.7 ms: 1.28x slower                                                                                                 |
| typing_runtime_protocols   | 196 us                                                                                                          | 251 us: 1.28x slower                                                                                                  |
| genshi_text                | 26.1 ms                                                                                                         | 33.7 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 10.5 ms                                                                                                         | 13.7 ms: 1.31x slower                                                                                                 |
| nbody                      | 117 ms                                                                                                          | 154 ms: 1.31x slower                                                                                                  |
| coverage                   | 105 ms                                                                                                          | 142 ms: 1.36x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (2): regex_effbot, async_tree_none

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.21x