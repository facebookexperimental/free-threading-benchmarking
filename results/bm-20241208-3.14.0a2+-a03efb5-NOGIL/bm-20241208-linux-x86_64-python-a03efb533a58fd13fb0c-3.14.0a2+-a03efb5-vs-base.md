# Results vs. base

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.248x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 411 ms                                                                                                            | 589 ms: 1.43x slower                                                                                                    |
| docutils       | 3.58 sec                                                                                                          | 4.24 sec: 1.19x slower                                                                                                  |
| html5lib       | 82.5 ms                                                                                                           | 123 ms: 1.48x slower                                                                                                    |
| sphinx         | 1.39 sec                                                                                                          | 1.65 sec: 1.18x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.31x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 707 ms                                                                                                            | 725 ms: 1.03x slower                                                                                                    |
| coroutines                 | 31.0 ms                                                                                                           | 34.4 ms: 1.11x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 681 ms                                                                                                            | 762 ms: 1.12x slower                                                                                                    |
| async_tree_io_tg           | 855 ms                                                                                                            | 1.03 sec: 1.21x slower                                                                                                  |
| async_generators           | 523 ms                                                                                                            | 644 ms: 1.23x slower                                                                                                    |
| async_tree_none_tg         | 366 ms                                                                                                            | 458 ms: 1.25x slower                                                                                                    |
| async_tree_memoization_tg  | 479 ms                                                                                                            | 600 ms: 1.25x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 668 ms                                                                                                            | 841 ms: 1.26x slower                                                                                                    |
| async_tree_io              | 839 ms                                                                                                            | 1.08 sec: 1.29x slower                                                                                                  |
| async_tree_memoization     | 481 ms                                                                                                            | 648 ms: 1.35x slower                                                                                                    |
| async_tree_none            | 380 ms                                                                                                            | 519 ms: 1.37x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.22x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 121 ms                                                                                                            | 173 ms: 1.42x slower                                                                                                    |
| float          | 112 ms                                                                                                            | 175 ms: 1.56x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.31x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 32.6 ms                                                                                                           | 34.0 ms: 1.04x slower                                                                                                   |
| regex_dna      | 270 ms                                                                                                            | 285 ms: 1.06x slower                                                                                                    |
| regex_compile  | 164 ms                                                                                                            | 224 ms: 1.37x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 33.4 us                                                                                                           | 36.6 us: 1.09x slower                                                                                                   |
| xml_etree_parse      | 199 ms                                                                                                            | 218 ms: 1.10x slower                                                                                                    |
| xml_etree_generate   | 113 ms                                                                                                            | 140 ms: 1.24x slower                                                                                                    |
| tomli_loads          | 2.70 sec                                                                                                          | 3.39 sec: 1.25x slower                                                                                                  |
| json_dumps           | 15.1 ms                                                                                                           | 19.0 ms: 1.25x slower                                                                                                   |
| xml_etree_process    | 78.3 ms                                                                                                           | 100 ms: 1.28x slower                                                                                                    |
| unpickle_pure_python | 281 us                                                                                                            | 404 us: 1.44x slower                                                                                                    |
| pickle_pure_python   | 427 us                                                                                                            | 622 us: 1.46x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.23x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 24.0 ms                                                                                                           | 32.5 ms: 1.35x slower                                                                                                   |
| python_startup_no_site | 13.9 ms                                                                                                           | 19.3 ms: 1.39x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.37x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 64.8 ms                                                                                                           | 84.8 ms: 1.31x slower                                                                                                   |
| genshi_text     | 29.1 ms                                                                                                           | 40.0 ms: 1.37x slower                                                                                                   |
| django_template | 45.2 ms                                                                                                           | 63.5 ms: 1.41x slower                                                                                                   |
| mako            | 16.6 ms                                                                                                           | 26.8 ms: 1.62x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.42x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json | results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.38 ms                                                                                                           | 5.60 ms: 1.32x faster                                                                                                   |
| create_gc_cycles           | 3.43 ms                                                                                                           | 3.12 ms: 1.10x faster                                                                                                   |
| asyncio_websockets         | 707 ms                                                                                                            | 725 ms: 1.03x slower                                                                                                    |
| regex_v8                   | 32.6 ms                                                                                                           | 34.0 ms: 1.04x slower                                                                                                   |
| regex_dna                  | 270 ms                                                                                                            | 285 ms: 1.06x slower                                                                                                    |
| sqlite_synth               | 3.71 us                                                                                                           | 4.01 us: 1.08x slower                                                                                                   |
| bench_mp_pool              | 85.0 ms                                                                                                           | 92.9 ms: 1.09x slower                                                                                                   |
| json                       | 6.28 ms                                                                                                           | 6.87 ms: 1.09x slower                                                                                                   |
| json_loads                 | 33.4 us                                                                                                           | 36.6 us: 1.09x slower                                                                                                   |
| xml_etree_parse            | 199 ms                                                                                                            | 218 ms: 1.10x slower                                                                                                    |
| coroutines                 | 31.0 ms                                                                                                           | 34.4 ms: 1.11x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 681 ms                                                                                                            | 762 ms: 1.12x slower                                                                                                    |
| spectral_norm              | 155 ms                                                                                                            | 176 ms: 1.14x slower                                                                                                    |
| telco                      | 10.5 ms                                                                                                           | 11.9 ms: 1.14x slower                                                                                                   |
| meteor_contest             | 152 ms                                                                                                            | 173 ms: 1.14x slower                                                                                                    |
| connected_components       | 791 ms                                                                                                            | 905 ms: 1.14x slower                                                                                                    |
| k_core                     | 3.84 sec                                                                                                          | 4.46 sec: 1.16x slower                                                                                                  |
| bench_thread_pool          | 2.72 ms                                                                                                           | 3.22 ms: 1.18x slower                                                                                                   |
| sphinx                     | 1.39 sec                                                                                                          | 1.65 sec: 1.18x slower                                                                                                  |
| shortest_path              | 847 ms                                                                                                            | 1.00 sec: 1.18x slower                                                                                                  |
| docutils                   | 3.58 sec                                                                                                          | 4.24 sec: 1.19x slower                                                                                                  |
| scimark_fft                | 470 ms                                                                                                            | 559 ms: 1.19x slower                                                                                                    |
| deepcopy_reduce            | 3.64 us                                                                                                           | 4.36 us: 1.20x slower                                                                                                   |
| coverage                   | 112 ms                                                                                                            | 134 ms: 1.20x slower                                                                                                    |
| async_tree_io_tg           | 855 ms                                                                                                            | 1.03 sec: 1.21x slower                                                                                                  |
| scimark_sparse_mat_mult    | 6.36 ms                                                                                                           | 7.72 ms: 1.21x slower                                                                                                   |
| sqlglot_optimize           | 71.0 ms                                                                                                           | 86.2 ms: 1.21x slower                                                                                                   |
| sqlglot_normalize          | 139 ms                                                                                                            | 170 ms: 1.22x slower                                                                                                    |
| pathlib                    | 25.8 ms                                                                                                           | 31.7 ms: 1.23x slower                                                                                                   |
| async_generators           | 523 ms                                                                                                            | 644 ms: 1.23x slower                                                                                                    |
| xml_etree_generate         | 113 ms                                                                                                            | 140 ms: 1.24x slower                                                                                                    |
| bpe_tokeniser              | 5.73 sec                                                                                                          | 7.11 sec: 1.24x slower                                                                                                  |
| nqueens                    | 101 ms                                                                                                            | 126 ms: 1.25x slower                                                                                                    |
| async_tree_none_tg         | 366 ms                                                                                                            | 458 ms: 1.25x slower                                                                                                    |
| async_tree_memoization_tg  | 479 ms                                                                                                            | 600 ms: 1.25x slower                                                                                                    |
| tomli_loads                | 2.70 sec                                                                                                          | 3.39 sec: 1.25x slower                                                                                                  |
| json_dumps                 | 15.1 ms                                                                                                           | 19.0 ms: 1.25x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 668 ms                                                                                                            | 841 ms: 1.26x slower                                                                                                    |
| mdp                        | 3.54 sec                                                                                                          | 4.48 sec: 1.27x slower                                                                                                  |
| xml_etree_process          | 78.3 ms                                                                                                           | 100 ms: 1.28x slower                                                                                                    |
| deepcopy                   | 344 us                                                                                                            | 441 us: 1.28x slower                                                                                                    |
| async_tree_io              | 839 ms                                                                                                            | 1.08 sec: 1.29x slower                                                                                                  |
| many_optionals             | 1.06 ms                                                                                                           | 1.38 ms: 1.30x slower                                                                                                   |
| dulwich_log                | 93.4 ms                                                                                                           | 122 ms: 1.30x slower                                                                                                    |
| deepcopy_memo              | 38.2 us                                                                                                           | 50.0 us: 1.31x slower                                                                                                   |
| genshi_xml                 | 64.8 ms                                                                                                           | 84.8 ms: 1.31x slower                                                                                                   |
| crypto_pyaes               | 92.9 ms                                                                                                           | 122 ms: 1.32x slower                                                                                                    |
| typing_runtime_protocols   | 211 us                                                                                                            | 279 us: 1.32x slower                                                                                                    |
| pprint_safe_repr           | 954 ms                                                                                                            | 1.26 sec: 1.32x slower                                                                                                  |
| pycparser                  | 1.45 sec                                                                                                          | 1.94 sec: 1.34x slower                                                                                                  |
| async_tree_memoization     | 481 ms                                                                                                            | 648 ms: 1.35x slower                                                                                                    |
| python_startup             | 24.0 ms                                                                                                           | 32.5 ms: 1.35x slower                                                                                                   |
| generators                 | 38.4 ms                                                                                                           | 51.9 ms: 1.35x slower                                                                                                   |
| async_tree_none            | 380 ms                                                                                                            | 519 ms: 1.37x slower                                                                                                    |
| regex_compile              | 164 ms                                                                                                            | 224 ms: 1.37x slower                                                                                                    |
| genshi_text                | 29.1 ms                                                                                                           | 40.0 ms: 1.37x slower                                                                                                   |
| sympy_integrate            | 27.6 ms                                                                                                           | 38.1 ms: 1.38x slower                                                                                                   |
| pylint                     | 377 ms                                                                                                            | 523 ms: 1.39x slower                                                                                                    |
| python_startup_no_site     | 13.9 ms                                                                                                           | 19.3 ms: 1.39x slower                                                                                                   |
| pprint_pformat             | 1.92 sec                                                                                                          | 2.68 sec: 1.39x slower                                                                                                  |
| django_template            | 45.2 ms                                                                                                           | 63.5 ms: 1.41x slower                                                                                                   |
| fannkuch                   | 484 ms                                                                                                            | 683 ms: 1.41x slower                                                                                                    |
| nbody                      | 121 ms                                                                                                            | 173 ms: 1.42x slower                                                                                                    |
| 2to3                       | 411 ms                                                                                                            | 589 ms: 1.43x slower                                                                                                    |
| unpickle_pure_python       | 281 us                                                                                                            | 404 us: 1.44x slower                                                                                                    |
| subparsers                 | 29.0 ms                                                                                                           | 41.8 ms: 1.44x slower                                                                                                   |
| pickle_pure_python         | 427 us                                                                                                            | 622 us: 1.46x slower                                                                                                    |
| comprehensions             | 21.2 us                                                                                                           | 30.9 us: 1.46x slower                                                                                                   |
| scimark_lu                 | 151 ms                                                                                                            | 222 ms: 1.47x slower                                                                                                    |
| pyflate                    | 662 ms                                                                                                            | 980 ms: 1.48x slower                                                                                                    |
| html5lib                   | 82.5 ms                                                                                                           | 123 ms: 1.48x slower                                                                                                    |
| thrift                     | 985 us                                                                                                            | 1.46 ms: 1.48x slower                                                                                                   |
| chaos                      | 81.7 ms                                                                                                           | 125 ms: 1.53x slower                                                                                                    |
| richards_super             | 66.9 ms                                                                                                           | 103 ms: 1.54x slower                                                                                                    |
| logging_silent             | 139 ns                                                                                                            | 215 ns: 1.55x slower                                                                                                    |
| sympy_str                  | 359 ms                                                                                                            | 559 ms: 1.56x slower                                                                                                    |
| hexiom                     | 8.18 ms                                                                                                           | 12.8 ms: 1.56x slower                                                                                                   |
| float                      | 112 ms                                                                                                            | 175 ms: 1.56x slower                                                                                                    |
| richards                   | 57.7 ms                                                                                                           | 90.9 ms: 1.58x slower                                                                                                   |
| scimark_monte_carlo        | 92.2 ms                                                                                                           | 147 ms: 1.60x slower                                                                                                    |
| sqlalchemy_declarative     | 174 ms                                                                                                            | 279 ms: 1.61x slower                                                                                                    |
| logging_simple             | 8.16 us                                                                                                           | 13.2 us: 1.61x slower                                                                                                   |
| mako                       | 16.6 ms                                                                                                           | 26.8 ms: 1.62x slower                                                                                                   |
| logging_format             | 8.77 us                                                                                                           | 14.9 us: 1.70x slower                                                                                                   |
| sqlalchemy_imperative      | 21.4 ms                                                                                                           | 37.3 ms: 1.74x slower                                                                                                   |
| sqlglot_transpile          | 2.18 ms                                                                                                           | 3.83 ms: 1.76x slower                                                                                                   |
| scimark_sor                | 158 ms                                                                                                            | 285 ms: 1.80x slower                                                                                                    |
| raytrace                   | 345 ms                                                                                                            | 623 ms: 1.81x slower                                                                                                    |
| sqlglot_parse              | 1.66 ms                                                                                                           | 3.15 ms: 1.89x slower                                                                                                   |
| sympy_expand               | 571 ms                                                                                                            | 1.09 sec: 1.91x slower                                                                                                  |
| go                         | 151 ms                                                                                                            | 310 ms: 2.06x slower                                                                                                    |
| sympy_sum                  | 192 ms                                                                                                            | 429 ms: 2.23x slower                                                                                                    |
| deltablue                  | 4.17 ms                                                                                                           | 9.46 ms: 2.27x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.33x slower                                                                                                            |

Benchmark hidden because not significant (3): regex_effbot, xml_etree_iterparse, pidigits

- Geometric mean (including insignificant results): 1.248x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.18x