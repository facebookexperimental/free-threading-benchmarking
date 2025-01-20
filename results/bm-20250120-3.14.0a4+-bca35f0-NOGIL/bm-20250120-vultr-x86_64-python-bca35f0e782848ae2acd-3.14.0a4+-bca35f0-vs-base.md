# Results vs. base

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.139x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 305 ms: 1.21x slower                                                                                                    |
| docutils       | 2.56 sec                                                                                                          | 2.82 sec: 1.10x slower                                                                                                  |
| sphinx         | 983 ms                                                                                                            | 1.13 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 612 ms                                                                                                            | 579 ms: 1.06x faster                                                                                                    |
| async_tree_none_tg         | 255 ms                                                                                                            | 243 ms: 1.05x faster                                                                                                    |
| asyncio_websockets         | 523 ms                                                                                                            | 519 ms: 1.01x faster                                                                                                    |
| async_tree_memoization_tg  | 302 ms                                                                                                            | 312 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 474 ms                                                                                                            | 497 ms: 1.05x slower                                                                                                    |
| async_tree_none            | 272 ms                                                                                                            | 287 ms: 1.06x slower                                                                                                    |
| async_tree_memoization     | 326 ms                                                                                                            | 351 ms: 1.08x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                                                            | 535 ms: 1.08x slower                                                                                                    |
| coroutines                 | 21.4 ms                                                                                                           | 23.9 ms: 1.12x slower                                                                                                   |
| async_generators           | 324 ms                                                                                                            | 366 ms: 1.13x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                            | 205 ms: 1.05x slower                                                                                                    |
| float          | 71.9 ms                                                                                                           | 77.3 ms: 1.07x slower                                                                                                   |
| nbody          | 89.5 ms                                                                                                           | 128 ms: 1.43x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.0 ms                                                                                                           | 24.9 ms: 1.08x slower                                                                                                   |
| regex_dna      | 168 ms                                                                                                            | 188 ms: 1.12x slower                                                                                                    |
| regex_effbot   | 2.55 ms                                                                                                           | 2.92 ms: 1.15x slower                                                                                                   |
| regex_compile  | 126 ms                                                                                                            | 150 ms: 1.19x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 27.8 us                                                                                                           | 30.2 us: 1.09x slower                                                                                                   |
| json_dumps           | 11.5 ms                                                                                                           | 13.0 ms: 1.13x slower                                                                                                   |
| xml_etree_generate   | 84.8 ms                                                                                                           | 95.8 ms: 1.13x slower                                                                                                   |
| xml_etree_process    | 59.7 ms                                                                                                           | 68.8 ms: 1.15x slower                                                                                                   |
| unpickle_pure_python | 210 us                                                                                                            | 250 us: 1.19x slower                                                                                                    |
| pickle_pure_python   | 312 us                                                                                                            | 373 us: 1.19x slower                                                                                                    |
| tomli_loads          | 1.90 sec                                                                                                          | 2.34 sec: 1.23x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| python_startup_no_site | 7.46 ms                                                                                                           | 9.57 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.2 ms                                                                                                           | 43.5 ms: 1.24x slower                                                                                                   |
| genshi_xml      | 48.3 ms                                                                                                           | 60.7 ms: 1.26x slower                                                                                                   |
| genshi_text     | 21.2 ms                                                                                                           | 27.7 ms: 1.30x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 15.6 ms: 1.32x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.28x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.34 ms: 1.37x faster                                                                                                   |
| gc_traversal               | 4.45 ms                                                                                                           | 3.69 ms: 1.21x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.05 us: 1.08x faster                                                                                                   |
| async_tree_io_tg           | 612 ms                                                                                                            | 579 ms: 1.06x faster                                                                                                    |
| async_tree_none_tg         | 255 ms                                                                                                            | 243 ms: 1.05x faster                                                                                                    |
| asyncio_websockets         | 523 ms                                                                                                            | 519 ms: 1.01x faster                                                                                                    |
| pathlib                    | 18.2 ms                                                                                                           | 18.6 ms: 1.03x slower                                                                                                   |
| async_tree_memoization_tg  | 302 ms                                                                                                            | 312 ms: 1.03x slower                                                                                                    |
| python_startup             | 14.7 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 474 ms                                                                                                            | 497 ms: 1.05x slower                                                                                                    |
| pidigits                   | 195 ms                                                                                                            | 205 ms: 1.05x slower                                                                                                    |
| async_tree_none            | 272 ms                                                                                                            | 287 ms: 1.06x slower                                                                                                    |
| bench_mp_pool              | 88.7 ms                                                                                                           | 94.7 ms: 1.07x slower                                                                                                   |
| json                       | 4.93 ms                                                                                                           | 5.29 ms: 1.07x slower                                                                                                   |
| float                      | 71.9 ms                                                                                                           | 77.3 ms: 1.07x slower                                                                                                   |
| async_tree_memoization     | 326 ms                                                                                                            | 351 ms: 1.08x slower                                                                                                    |
| pycparser                  | 1.10 sec                                                                                                          | 1.19 sec: 1.08x slower                                                                                                  |
| dulwich_log                | 76.0 ms                                                                                                           | 82.0 ms: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 496 ms                                                                                                            | 535 ms: 1.08x slower                                                                                                    |
| regex_v8                   | 23.0 ms                                                                                                           | 24.9 ms: 1.08x slower                                                                                                   |
| json_loads                 | 27.8 us                                                                                                           | 30.2 us: 1.09x slower                                                                                                   |
| docutils                   | 2.56 sec                                                                                                          | 2.82 sec: 1.10x slower                                                                                                  |
| bpe_tokeniser              | 4.18 sec                                                                                                          | 4.66 sec: 1.11x slower                                                                                                  |
| coroutines                 | 21.4 ms                                                                                                           | 23.9 ms: 1.12x slower                                                                                                   |
| spectral_norm              | 94.2 ms                                                                                                           | 105 ms: 1.12x slower                                                                                                    |
| generators                 | 28.1 ms                                                                                                           | 31.4 ms: 1.12x slower                                                                                                   |
| regex_dna                  | 168 ms                                                                                                            | 188 ms: 1.12x slower                                                                                                    |
| mdp                        | 2.47 sec                                                                                                          | 2.78 sec: 1.12x slower                                                                                                  |
| json_dumps                 | 11.5 ms                                                                                                           | 13.0 ms: 1.13x slower                                                                                                   |
| xml_etree_generate         | 84.8 ms                                                                                                           | 95.8 ms: 1.13x slower                                                                                                   |
| subparsers                 | 22.3 ms                                                                                                           | 25.1 ms: 1.13x slower                                                                                                   |
| pylint                     | 282 ms                                                                                                            | 318 ms: 1.13x slower                                                                                                    |
| k_core                     | 2.05 sec                                                                                                          | 2.32 sec: 1.13x slower                                                                                                  |
| async_generators           | 324 ms                                                                                                            | 366 ms: 1.13x slower                                                                                                    |
| regex_effbot               | 2.55 ms                                                                                                           | 2.92 ms: 1.15x slower                                                                                                   |
| sphinx                     | 983 ms                                                                                                            | 1.13 sec: 1.15x slower                                                                                                  |
| many_optionals             | 1.03 ms                                                                                                           | 1.17 ms: 1.15x slower                                                                                                   |
| xml_etree_process          | 59.7 ms                                                                                                           | 68.8 ms: 1.15x slower                                                                                                   |
| sqlglot_normalize          | 104 ms                                                                                                            | 121 ms: 1.17x slower                                                                                                    |
| telco                      | 7.17 ms                                                                                                           | 8.36 ms: 1.17x slower                                                                                                   |
| pprint_safe_repr           | 711 ms                                                                                                            | 831 ms: 1.17x slower                                                                                                    |
| logging_simple             | 6.31 us                                                                                                           | 7.39 us: 1.17x slower                                                                                                   |
| logging_silent             | 101 ns                                                                                                            | 119 ns: 1.18x slower                                                                                                    |
| sqlglot_optimize           | 52.1 ms                                                                                                           | 61.6 ms: 1.18x slower                                                                                                   |
| pyflate                    | 415 ms                                                                                                            | 492 ms: 1.19x slower                                                                                                    |
| pprint_pformat             | 1.44 sec                                                                                                          | 1.71 sec: 1.19x slower                                                                                                  |
| unpickle_pure_python       | 210 us                                                                                                            | 250 us: 1.19x slower                                                                                                    |
| regex_compile              | 126 ms                                                                                                            | 150 ms: 1.19x slower                                                                                                    |
| pickle_pure_python         | 312 us                                                                                                            | 373 us: 1.19x slower                                                                                                    |
| logging_format             | 7.07 us                                                                                                           | 8.45 us: 1.19x slower                                                                                                   |
| deepcopy                   | 261 us                                                                                                            | 311 us: 1.19x slower                                                                                                    |
| sympy_expand               | 459 ms                                                                                                            | 551 ms: 1.20x slower                                                                                                    |
| scimark_sor                | 111 ms                                                                                                            | 134 ms: 1.20x slower                                                                                                    |
| nqueens                    | 78.9 ms                                                                                                           | 95.0 ms: 1.21x slower                                                                                                   |
| 2to3                       | 252 ms                                                                                                            | 305 ms: 1.21x slower                                                                                                    |
| scimark_fft                | 315 ms                                                                                                            | 382 ms: 1.21x slower                                                                                                    |
| scimark_lu                 | 113 ms                                                                                                            | 137 ms: 1.21x slower                                                                                                    |
| sympy_sum                  | 153 ms                                                                                                            | 187 ms: 1.22x slower                                                                                                    |
| sympy_integrate            | 19.8 ms                                                                                                           | 24.2 ms: 1.22x slower                                                                                                   |
| coverage                   | 79.7 ms                                                                                                           | 97.5 ms: 1.22x slower                                                                                                   |
| sympy_str                  | 274 ms                                                                                                            | 336 ms: 1.23x slower                                                                                                    |
| thrift                     | 749 us                                                                                                            | 920 us: 1.23x slower                                                                                                    |
| tomli_loads                | 1.90 sec                                                                                                          | 2.34 sec: 1.23x slower                                                                                                  |
| django_template            | 35.2 ms                                                                                                           | 43.5 ms: 1.24x slower                                                                                                   |
| connected_components       | 393 ms                                                                                                            | 488 ms: 1.24x slower                                                                                                    |
| shortest_path              | 434 ms                                                                                                            | 540 ms: 1.25x slower                                                                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                                                           | 24.2 ms: 1.25x slower                                                                                                   |
| typing_runtime_protocols   | 159 us                                                                                                            | 198 us: 1.25x slower                                                                                                    |
| sqlglot_transpile          | 1.55 ms                                                                                                           | 1.94 ms: 1.25x slower                                                                                                   |
| genshi_xml                 | 48.3 ms                                                                                                           | 60.7 ms: 1.26x slower                                                                                                   |
| chaos                      | 54.9 ms                                                                                                           | 69.0 ms: 1.26x slower                                                                                                   |
| comprehensions             | 16.7 us                                                                                                           | 21.0 us: 1.26x slower                                                                                                   |
| fannkuch                   | 374 ms                                                                                                            | 472 ms: 1.26x slower                                                                                                    |
| go                         | 112 ms                                                                                                            | 141 ms: 1.26x slower                                                                                                    |
| deepcopy_reduce            | 2.62 us                                                                                                           | 3.32 us: 1.27x slower                                                                                                   |
| sqlalchemy_declarative     | 128 ms                                                                                                            | 164 ms: 1.28x slower                                                                                                    |
| hexiom                     | 5.73 ms                                                                                                           | 7.36 ms: 1.28x slower                                                                                                   |
| python_startup_no_site     | 7.46 ms                                                                                                           | 9.57 ms: 1.28x slower                                                                                                   |
| meteor_contest             | 100 ms                                                                                                            | 129 ms: 1.29x slower                                                                                                    |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.61 ms: 1.29x slower                                                                                                   |
| raytrace                   | 259 ms                                                                                                            | 335 ms: 1.29x slower                                                                                                    |
| deepcopy_memo              | 29.8 us                                                                                                           | 38.5 us: 1.29x slower                                                                                                   |
| crypto_pyaes               | 66.9 ms                                                                                                           | 86.8 ms: 1.30x slower                                                                                                   |
| genshi_text                | 21.2 ms                                                                                                           | 27.7 ms: 1.30x slower                                                                                                   |
| scimark_monte_carlo        | 62.8 ms                                                                                                           | 82.8 ms: 1.32x slower                                                                                                   |
| mako                       | 11.8 ms                                                                                                           | 15.6 ms: 1.32x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.07 ms                                                                                                           | 5.47 ms: 1.34x slower                                                                                                   |
| richards                   | 41.5 ms                                                                                                           | 56.7 ms: 1.37x slower                                                                                                   |
| richards_super             | 47.6 ms                                                                                                           | 66.0 ms: 1.39x slower                                                                                                   |
| nbody                      | 89.5 ms                                                                                                           | 128 ms: 1.43x slower                                                                                                    |
| deltablue                  | 3.12 ms                                                                                                           | 4.73 ms: 1.51x slower                                                                                                   |
| bench_thread_pool          | 1.04 ms                                                                                                           | 3.30 ms: 3.18x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_io, xml_etree_parse, xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: html5lib

- Geometric mean (including insignificant results): 1.139x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x