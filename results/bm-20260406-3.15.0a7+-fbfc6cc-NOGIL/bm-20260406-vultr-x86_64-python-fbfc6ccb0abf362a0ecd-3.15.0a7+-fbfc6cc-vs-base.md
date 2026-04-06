# Results vs. base

- fork: python
- ref: fbfc6ccb0abf362a0ecd
- machine: linux-x86_64
- commit hash: fbfc6cc
- commit date: 2026-04-06
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 283 ms: 1.12x slower                                                                                                    |
| docutils       | 2.48 sec                                                                                                          | 2.65 sec: 1.07x slower                                                                                                  |
| html5lib       | 59.6 ms                                                                                                           | 65.5 ms: 1.10x slower                                                                                                   |
| sphinx         | 977 ms                                                                                                            | 1.05 sec: 1.07x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                                                            | 514 ms: 1.06x faster                                                                                                    |
| coroutines                 | 24.0 ms                                                                                                           | 23.9 ms: 1.01x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                                                            | 509 ms: 1.05x slower                                                                                                    |
| async_tree_io_tg           | 579 ms                                                                                                            | 614 ms: 1.06x slower                                                                                                    |
| async_tree_memoization_tg  | 306 ms                                                                                                            | 327 ms: 1.07x slower                                                                                                    |
| async_tree_io              | 597 ms                                                                                                            | 642 ms: 1.08x slower                                                                                                    |
| async_tree_none_tg         | 247 ms                                                                                                            | 265 ms: 1.08x slower                                                                                                    |
| async_generators           | 344 ms                                                                                                            | 375 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 483 ms                                                                                                            | 536 ms: 1.11x slower                                                                                                    |
| async_tree_memoization     | 314 ms                                                                                                            | 358 ms: 1.14x slower                                                                                                    |
| async_tree_none            | 252 ms                                                                                                            | 292 ms: 1.16x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                            | 181 ms: 1.02x faster                                                                                                    |
| float          | 71.2 ms                                                                                                           | 74.5 ms: 1.05x slower                                                                                                   |
| nbody          | 95.6 ms                                                                                                           | 125 ms: 1.30x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                                                                           | 20.5 ms: 1.11x faster                                                                                                   |
| regex_effbot   | 2.89 ms                                                                                                           | 2.73 ms: 1.06x faster                                                                                                   |
| regex_dna      | 178 ms                                                                                                            | 169 ms: 1.06x faster                                                                                                    |
| regex_compile  | 125 ms                                                                                                            | 142 ms: 1.13x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.7 ms                                                                                                           | 86.8 ms: 1.02x slower                                                                                                   |
| json_loads           | 27.8 us                                                                                                           | 29.5 us: 1.06x slower                                                                                                   |
| tomli_loads          | 1.84 sec                                                                                                          | 1.96 sec: 1.06x slower                                                                                                  |
| pickle_pure_python   | 316 us                                                                                                            | 336 us: 1.06x slower                                                                                                    |
| unpickle_pure_python | 217 us                                                                                                            | 236 us: 1.09x slower                                                                                                    |
| json_dumps           | 9.85 ms                                                                                                           | 11.0 ms: 1.12x slower                                                                                                   |
| xml_etree_generate   | 84.4 ms                                                                                                           | 96.7 ms: 1.15x slower                                                                                                   |
| xml_etree_process    | 60.2 ms                                                                                                           | 69.1 ms: 1.15x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                                                           | 16.1 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.47 ms                                                                                                           | 9.86 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                                                           | 39.8 ms: 1.12x slower                                                                                                   |
| genshi_xml      | 49.3 ms                                                                                                           | 55.1 ms: 1.12x slower                                                                                                   |
| genshi_text     | 20.9 ms                                                                                                           | 25.7 ms: 1.23x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 15.9 ms: 1.31x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.19x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json | results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 278 ms                                                                                                            | 7.03 ms: 39.48x faster                                                                                                  |
| gc_traversal               | 4.30 ms                                                                                                           | 1.93 ms: 2.23x faster                                                                                                   |
| create_gc_cycles           | 1.88 ms                                                                                                           | 1.50 ms: 1.26x faster                                                                                                   |
| sqlite_synth               | 2.23 us                                                                                                           | 1.93 us: 1.16x faster                                                                                                   |
| regex_v8                   | 22.7 ms                                                                                                           | 20.5 ms: 1.11x faster                                                                                                   |
| regex_effbot               | 2.89 ms                                                                                                           | 2.73 ms: 1.06x faster                                                                                                   |
| asyncio_websockets         | 544 ms                                                                                                            | 514 ms: 1.06x faster                                                                                                    |
| regex_dna                  | 178 ms                                                                                                            | 169 ms: 1.06x faster                                                                                                    |
| pidigits                   | 184 ms                                                                                                            | 181 ms: 1.02x faster                                                                                                    |
| pathlib                    | 17.8 ms                                                                                                           | 17.4 ms: 1.02x faster                                                                                                   |
| coroutines                 | 24.0 ms                                                                                                           | 23.9 ms: 1.01x faster                                                                                                   |
| xml_etree_iterparse        | 84.7 ms                                                                                                           | 86.8 ms: 1.02x slower                                                                                                   |
| float                      | 71.2 ms                                                                                                           | 74.5 ms: 1.05x slower                                                                                                   |
| bpe_tokeniser              | 4.18 sec                                                                                                          | 4.39 sec: 1.05x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                                                            | 509 ms: 1.05x slower                                                                                                    |
| dulwich_log                | 67.4 ms                                                                                                           | 71.1 ms: 1.06x slower                                                                                                   |
| json_loads                 | 27.8 us                                                                                                           | 29.5 us: 1.06x slower                                                                                                   |
| pylint                     | 283 ms                                                                                                            | 300 ms: 1.06x slower                                                                                                    |
| async_tree_io_tg           | 579 ms                                                                                                            | 614 ms: 1.06x slower                                                                                                    |
| tomli_loads                | 1.84 sec                                                                                                          | 1.96 sec: 1.06x slower                                                                                                  |
| pickle_pure_python         | 316 us                                                                                                            | 336 us: 1.06x slower                                                                                                    |
| deltablue                  | 3.29 ms                                                                                                           | 3.49 ms: 1.06x slower                                                                                                   |
| docutils                   | 2.48 sec                                                                                                          | 2.65 sec: 1.07x slower                                                                                                  |
| async_tree_memoization_tg  | 306 ms                                                                                                            | 327 ms: 1.07x slower                                                                                                    |
| sphinx                     | 977 ms                                                                                                            | 1.05 sec: 1.07x slower                                                                                                  |
| async_tree_io              | 597 ms                                                                                                            | 642 ms: 1.08x slower                                                                                                    |
| async_tree_none_tg         | 247 ms                                                                                                            | 265 ms: 1.08x slower                                                                                                    |
| telco                      | 159 ms                                                                                                            | 172 ms: 1.09x slower                                                                                                    |
| sympy_expand               | 480 ms                                                                                                            | 522 ms: 1.09x slower                                                                                                    |
| logging_silent             | 98.0 ns                                                                                                           | 107 ns: 1.09x slower                                                                                                    |
| async_generators           | 344 ms                                                                                                            | 375 ms: 1.09x slower                                                                                                    |
| unpickle_pure_python       | 217 us                                                                                                            | 236 us: 1.09x slower                                                                                                    |
| many_optionals             | 938 us                                                                                                            | 1.02 ms: 1.09x slower                                                                                                   |
| pprint_safe_repr           | 726 ms                                                                                                            | 794 ms: 1.09x slower                                                                                                    |
| subparsers                 | 9.24 ms                                                                                                           | 10.1 ms: 1.10x slower                                                                                                   |
| bench_thread_pool          | 1.33 ms                                                                                                           | 1.46 ms: 1.10x slower                                                                                                   |
| html5lib                   | 59.6 ms                                                                                                           | 65.5 ms: 1.10x slower                                                                                                   |
| comprehensions             | 16.6 us                                                                                                           | 18.4 us: 1.11x slower                                                                                                   |
| deepcopy                   | 241 us                                                                                                            | 267 us: 1.11x slower                                                                                                    |
| sqlglot_v2_optimize        | 51.2 ms                                                                                                           | 56.8 ms: 1.11x slower                                                                                                   |
| deepcopy_reduce            | 2.62 us                                                                                                           | 2.90 us: 1.11x slower                                                                                                   |
| sympy_str                  | 280 ms                                                                                                            | 311 ms: 1.11x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 483 ms                                                                                                            | 536 ms: 1.11x slower                                                                                                    |
| sqlglot_v2_normalize       | 103 ms                                                                                                            | 115 ms: 1.11x slower                                                                                                    |
| scimark_sor                | 110 ms                                                                                                            | 122 ms: 1.11x slower                                                                                                    |
| django_template            | 35.7 ms                                                                                                           | 39.8 ms: 1.12x slower                                                                                                   |
| genshi_xml                 | 49.3 ms                                                                                                           | 55.1 ms: 1.12x slower                                                                                                   |
| pprint_pformat             | 1.48 sec                                                                                                          | 1.65 sec: 1.12x slower                                                                                                  |
| generators                 | 28.8 ms                                                                                                           | 32.2 ms: 1.12x slower                                                                                                   |
| sympy_sum                  | 159 ms                                                                                                            | 178 ms: 1.12x slower                                                                                                    |
| scimark_fft                | 312 ms                                                                                                            | 350 ms: 1.12x slower                                                                                                    |
| json_dumps                 | 9.85 ms                                                                                                           | 11.0 ms: 1.12x slower                                                                                                   |
| 2to3                       | 252 ms                                                                                                            | 283 ms: 1.12x slower                                                                                                    |
| mdp                        | 1.16 sec                                                                                                          | 1.31 sec: 1.12x slower                                                                                                  |
| sympy_integrate            | 19.3 ms                                                                                                           | 21.9 ms: 1.13x slower                                                                                                   |
| pyflate                    | 414 ms                                                                                                            | 469 ms: 1.13x slower                                                                                                    |
| logging_simple             | 5.93 us                                                                                                           | 6.72 us: 1.13x slower                                                                                                   |
| regex_compile              | 125 ms                                                                                                            | 142 ms: 1.13x slower                                                                                                    |
| async_tree_memoization     | 314 ms                                                                                                            | 358 ms: 1.14x slower                                                                                                    |
| logging_format             | 6.69 us                                                                                                           | 7.64 us: 1.14x slower                                                                                                   |
| deepcopy_memo              | 27.7 us                                                                                                           | 31.6 us: 1.14x slower                                                                                                   |
| xml_etree_generate         | 84.4 ms                                                                                                           | 96.7 ms: 1.15x slower                                                                                                   |
| hexiom                     | 5.80 ms                                                                                                           | 6.66 ms: 1.15x slower                                                                                                   |
| chaos                      | 53.7 ms                                                                                                           | 61.7 ms: 1.15x slower                                                                                                   |
| xml_etree_process          | 60.2 ms                                                                                                           | 69.1 ms: 1.15x slower                                                                                                   |
| nqueens                    | 75.9 ms                                                                                                           | 87.3 ms: 1.15x slower                                                                                                   |
| async_tree_none            | 252 ms                                                                                                            | 292 ms: 1.16x slower                                                                                                    |
| go                         | 104 ms                                                                                                            | 121 ms: 1.16x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                           | 1.78 ms: 1.17x slower                                                                                                   |
| scimark_lu                 | 108 ms                                                                                                            | 126 ms: 1.17x slower                                                                                                    |
| fannkuch                   | 390 ms                                                                                                            | 458 ms: 1.17x slower                                                                                                    |
| sqlglot_v2_parse           | 1.22 ms                                                                                                           | 1.45 ms: 1.18x slower                                                                                                   |
| k_core                     | 1.89 sec                                                                                                          | 2.24 sec: 1.19x slower                                                                                                  |
| raytrace                   | 253 ms                                                                                                            | 302 ms: 1.19x slower                                                                                                    |
| typing_runtime_protocols   | 159 us                                                                                                            | 191 us: 1.20x slower                                                                                                    |
| spectral_norm              | 94.0 ms                                                                                                           | 113 ms: 1.20x slower                                                                                                    |
| meteor_contest             | 102 ms                                                                                                            | 123 ms: 1.20x slower                                                                                                    |
| thrift                     | 765 us                                                                                                            | 924 us: 1.21x slower                                                                                                    |
| richards_super             | 49.1 ms                                                                                                           | 59.4 ms: 1.21x slower                                                                                                   |
| shortest_path              | 438 ms                                                                                                            | 531 ms: 1.21x slower                                                                                                    |
| richards                   | 42.6 ms                                                                                                           | 52.1 ms: 1.22x slower                                                                                                   |
| genshi_text                | 20.9 ms                                                                                                           | 25.7 ms: 1.23x slower                                                                                                   |
| scimark_monte_carlo        | 63.5 ms                                                                                                           | 78.4 ms: 1.23x slower                                                                                                   |
| connected_components       | 390 ms                                                                                                            | 486 ms: 1.24x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.45 ms                                                                                                           | 5.55 ms: 1.25x slower                                                                                                   |
| python_startup             | 12.7 ms                                                                                                           | 16.1 ms: 1.27x slower                                                                                                   |
| crypto_pyaes               | 69.1 ms                                                                                                           | 88.2 ms: 1.28x slower                                                                                                   |
| nbody                      | 95.6 ms                                                                                                           | 125 ms: 1.30x slower                                                                                                    |
| mako                       | 12.1 ms                                                                                                           | 15.9 ms: 1.31x slower                                                                                                   |
| python_startup_no_site     | 7.47 ms                                                                                                           | 9.86 ms: 1.32x slower                                                                                                   |
| coverage                   | 82.1 ms                                                                                                           | 110 ms: 1.34x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (3): pycparser, json, xml_etree_parse

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.21x