# Results vs. base

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: linux-x86_64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                                                            | 284 ms: 1.11x slower                                                                                                    |
| docutils       | 2.50 sec                                                                                                          | 2.63 sec: 1.05x slower                                                                                                  |
| html5lib       | 60.1 ms                                                                                                           | 65.7 ms: 1.09x slower                                                                                                   |
| sphinx         | 972 ms                                                                                                            | 1.05 sec: 1.08x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                                                            | 508 ms: 1.07x faster                                                                                                    |
| async_tree_io_tg           | 597 ms                                                                                                            | 612 ms: 1.03x slower                                                                                                    |
| async_tree_none_tg         | 253 ms                                                                                                            | 262 ms: 1.04x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 488 ms                                                                                                            | 511 ms: 1.05x slower                                                                                                    |
| async_tree_memoization_tg  | 307 ms                                                                                                            | 325 ms: 1.06x slower                                                                                                    |
| async_tree_io              | 585 ms                                                                                                            | 638 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                            | 538 ms: 1.10x slower                                                                                                    |
| async_generators           | 342 ms                                                                                                            | 380 ms: 1.11x slower                                                                                                    |
| async_tree_memoization     | 315 ms                                                                                                            | 357 ms: 1.13x slower                                                                                                    |
| async_tree_none            | 246 ms                                                                                                            | 292 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                            | 192 ms: 1.02x slower                                                                                                    |
| float          | 71.0 ms                                                                                                           | 73.6 ms: 1.04x slower                                                                                                   |
| nbody          | 92.8 ms                                                                                                           | 123 ms: 1.32x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.87 ms                                                                                                           | 2.74 ms: 1.05x faster                                                                                                   |
| regex_v8       | 21.7 ms                                                                                                           | 21.0 ms: 1.03x faster                                                                                                   |
| regex_dna      | 172 ms                                                                                                            | 175 ms: 1.02x slower                                                                                                    |
| regex_compile  | 124 ms                                                                                                            | 141 ms: 1.13x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.4 ms                                                                                                           | 87.3 ms: 1.03x slower                                                                                                   |
| tomli_loads          | 1.82 sec                                                                                                          | 1.92 sec: 1.05x slower                                                                                                  |
| pickle_pure_python   | 317 us                                                                                                            | 338 us: 1.06x slower                                                                                                    |
| json_loads           | 27.3 us                                                                                                           | 29.3 us: 1.07x slower                                                                                                   |
| unpickle_pure_python | 216 us                                                                                                            | 237 us: 1.10x slower                                                                                                    |
| xml_etree_generate   | 85.2 ms                                                                                                           | 95.5 ms: 1.12x slower                                                                                                   |
| xml_etree_process    | 60.2 ms                                                                                                           | 68.4 ms: 1.13x slower                                                                                                   |
| json_dumps           | 9.80 ms                                                                                                           | 11.3 ms: 1.15x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                                                           | 16.2 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.49 ms                                                                                                           | 9.93 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 50.8 ms                                                                                                           | 54.0 ms: 1.06x slower                                                                                                   |
| django_template | 35.7 ms                                                                                                           | 39.2 ms: 1.10x slower                                                                                                   |
| genshi_text     | 21.7 ms                                                                                                           | 25.3 ms: 1.17x slower                                                                                                   |
| mako            | 12.2 ms                                                                                                           | 15.6 ms: 1.28x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.15x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json | results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 235 ms                                                                                                            | 7.05 ms: 33.31x faster                                                                                                  |
| gc_traversal               | 4.28 ms                                                                                                           | 1.97 ms: 2.17x faster                                                                                                   |
| create_gc_cycles           | 1.92 ms                                                                                                           | 1.53 ms: 1.25x faster                                                                                                   |
| sqlite_synth               | 2.17 us                                                                                                           | 1.94 us: 1.11x faster                                                                                                   |
| asyncio_websockets         | 544 ms                                                                                                            | 508 ms: 1.07x faster                                                                                                    |
| regex_effbot               | 2.87 ms                                                                                                           | 2.74 ms: 1.05x faster                                                                                                   |
| regex_v8                   | 21.7 ms                                                                                                           | 21.0 ms: 1.03x faster                                                                                                   |
| json                       | 5.03 ms                                                                                                           | 5.06 ms: 1.01x slower                                                                                                   |
| pathlib                    | 17.4 ms                                                                                                           | 17.7 ms: 1.01x slower                                                                                                   |
| regex_dna                  | 172 ms                                                                                                            | 175 ms: 1.02x slower                                                                                                    |
| logging_silent             | 100 ns                                                                                                            | 102 ns: 1.02x slower                                                                                                    |
| dulwich_log                | 68.7 ms                                                                                                           | 70.2 ms: 1.02x slower                                                                                                   |
| pidigits                   | 187 ms                                                                                                            | 192 ms: 1.02x slower                                                                                                    |
| async_tree_io_tg           | 597 ms                                                                                                            | 612 ms: 1.03x slower                                                                                                    |
| pycparser                  | 1.08 sec                                                                                                          | 1.11 sec: 1.03x slower                                                                                                  |
| deltablue                  | 3.37 ms                                                                                                           | 3.47 ms: 1.03x slower                                                                                                   |
| xml_etree_iterparse        | 84.4 ms                                                                                                           | 87.3 ms: 1.03x slower                                                                                                   |
| async_tree_none_tg         | 253 ms                                                                                                            | 262 ms: 1.04x slower                                                                                                    |
| float                      | 71.0 ms                                                                                                           | 73.6 ms: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 488 ms                                                                                                            | 511 ms: 1.05x slower                                                                                                    |
| pylint                     | 283 ms                                                                                                            | 297 ms: 1.05x slower                                                                                                    |
| docutils                   | 2.50 sec                                                                                                          | 2.63 sec: 1.05x slower                                                                                                  |
| tomli_loads                | 1.82 sec                                                                                                          | 1.92 sec: 1.05x slower                                                                                                  |
| bpe_tokeniser              | 4.12 sec                                                                                                          | 4.37 sec: 1.06x slower                                                                                                  |
| async_tree_memoization_tg  | 307 ms                                                                                                            | 325 ms: 1.06x slower                                                                                                    |
| genshi_xml                 | 50.8 ms                                                                                                           | 54.0 ms: 1.06x slower                                                                                                   |
| pickle_pure_python         | 317 us                                                                                                            | 338 us: 1.06x slower                                                                                                    |
| json_loads                 | 27.3 us                                                                                                           | 29.3 us: 1.07x slower                                                                                                   |
| telco                      | 159 ms                                                                                                            | 171 ms: 1.07x slower                                                                                                    |
| sphinx                     | 972 ms                                                                                                            | 1.05 sec: 1.08x slower                                                                                                  |
| bench_thread_pool          | 1.33 ms                                                                                                           | 1.46 ms: 1.09x slower                                                                                                   |
| async_tree_io              | 585 ms                                                                                                            | 638 ms: 1.09x slower                                                                                                    |
| comprehensions             | 16.3 us                                                                                                           | 17.9 us: 1.09x slower                                                                                                   |
| html5lib                   | 60.1 ms                                                                                                           | 65.7 ms: 1.09x slower                                                                                                   |
| many_optionals             | 934 us                                                                                                            | 1.02 ms: 1.10x slower                                                                                                   |
| pprint_safe_repr           | 730 ms                                                                                                            | 800 ms: 1.10x slower                                                                                                    |
| sympy_expand               | 480 ms                                                                                                            | 527 ms: 1.10x slower                                                                                                    |
| unpickle_pure_python       | 216 us                                                                                                            | 237 us: 1.10x slower                                                                                                    |
| subparsers                 | 9.32 ms                                                                                                           | 10.2 ms: 1.10x slower                                                                                                   |
| django_template            | 35.7 ms                                                                                                           | 39.2 ms: 1.10x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                            | 538 ms: 1.10x slower                                                                                                    |
| scimark_sor                | 111 ms                                                                                                            | 122 ms: 1.11x slower                                                                                                    |
| sqlglot_v2_optimize        | 51.2 ms                                                                                                           | 56.7 ms: 1.11x slower                                                                                                   |
| async_generators           | 342 ms                                                                                                            | 380 ms: 1.11x slower                                                                                                    |
| pprint_pformat             | 1.49 sec                                                                                                          | 1.66 sec: 1.11x slower                                                                                                  |
| sympy_str                  | 279 ms                                                                                                            | 311 ms: 1.11x slower                                                                                                    |
| 2to3                       | 255 ms                                                                                                            | 284 ms: 1.11x slower                                                                                                    |
| sympy_sum                  | 159 ms                                                                                                            | 177 ms: 1.12x slower                                                                                                    |
| sqlglot_v2_normalize       | 102 ms                                                                                                            | 114 ms: 1.12x slower                                                                                                    |
| deepcopy                   | 239 us                                                                                                            | 268 us: 1.12x slower                                                                                                    |
| xml_etree_generate         | 85.2 ms                                                                                                           | 95.5 ms: 1.12x slower                                                                                                   |
| hexiom                     | 5.89 ms                                                                                                           | 6.61 ms: 1.12x slower                                                                                                   |
| deepcopy_memo              | 27.8 us                                                                                                           | 31.2 us: 1.12x slower                                                                                                   |
| deepcopy_reduce            | 2.62 us                                                                                                           | 2.95 us: 1.13x slower                                                                                                   |
| scimark_fft                | 313 ms                                                                                                            | 353 ms: 1.13x slower                                                                                                    |
| pyflate                    | 411 ms                                                                                                            | 463 ms: 1.13x slower                                                                                                    |
| sympy_integrate            | 19.2 ms                                                                                                           | 21.7 ms: 1.13x slower                                                                                                   |
| logging_simple             | 5.97 us                                                                                                           | 6.74 us: 1.13x slower                                                                                                   |
| regex_compile              | 124 ms                                                                                                            | 141 ms: 1.13x slower                                                                                                    |
| chaos                      | 54.9 ms                                                                                                           | 62.3 ms: 1.13x slower                                                                                                   |
| async_tree_memoization     | 315 ms                                                                                                            | 357 ms: 1.13x slower                                                                                                    |
| xml_etree_process          | 60.2 ms                                                                                                           | 68.4 ms: 1.13x slower                                                                                                   |
| go                         | 106 ms                                                                                                            | 121 ms: 1.14x slower                                                                                                    |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| json_dumps                 | 9.80 ms                                                                                                           | 11.3 ms: 1.15x slower                                                                                                   |
| thrift                     | 769 us                                                                                                            | 890 us: 1.16x slower                                                                                                    |
| generators                 | 28.4 ms                                                                                                           | 33.0 ms: 1.16x slower                                                                                                   |
| sqlglot_v2_parse           | 1.18 ms                                                                                                           | 1.37 ms: 1.16x slower                                                                                                   |
| logging_format             | 6.60 us                                                                                                           | 7.69 us: 1.16x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                           | 1.72 ms: 1.17x slower                                                                                                   |
| scimark_lu                 | 108 ms                                                                                                            | 126 ms: 1.17x slower                                                                                                    |
| genshi_text                | 21.7 ms                                                                                                           | 25.3 ms: 1.17x slower                                                                                                   |
| nqueens                    | 75.0 ms                                                                                                           | 87.5 ms: 1.17x slower                                                                                                   |
| richards_super             | 49.8 ms                                                                                                           | 58.5 ms: 1.18x slower                                                                                                   |
| spectral_norm              | 90.9 ms                                                                                                           | 107 ms: 1.18x slower                                                                                                    |
| k_core                     | 1.89 sec                                                                                                          | 2.23 sec: 1.18x slower                                                                                                  |
| raytrace                   | 255 ms                                                                                                            | 302 ms: 1.18x slower                                                                                                    |
| async_tree_none            | 246 ms                                                                                                            | 292 ms: 1.19x slower                                                                                                    |
| richards                   | 43.2 ms                                                                                                           | 51.4 ms: 1.19x slower                                                                                                   |
| fannkuch                   | 383 ms                                                                                                            | 457 ms: 1.19x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.52 ms                                                                                                           | 5.44 ms: 1.20x slower                                                                                                   |
| typing_runtime_protocols   | 159 us                                                                                                            | 193 us: 1.21x slower                                                                                                    |
| shortest_path              | 433 ms                                                                                                            | 531 ms: 1.23x slower                                                                                                    |
| connected_components       | 391 ms                                                                                                            | 483 ms: 1.24x slower                                                                                                    |
| meteor_contest             | 101 ms                                                                                                            | 126 ms: 1.25x slower                                                                                                    |
| scimark_monte_carlo        | 62.5 ms                                                                                                           | 78.8 ms: 1.26x slower                                                                                                   |
| python_startup             | 12.7 ms                                                                                                           | 16.2 ms: 1.27x slower                                                                                                   |
| crypto_pyaes               | 69.3 ms                                                                                                           | 88.3 ms: 1.27x slower                                                                                                   |
| mako                       | 12.2 ms                                                                                                           | 15.6 ms: 1.28x slower                                                                                                   |
| nbody                      | 92.8 ms                                                                                                           | 123 ms: 1.32x slower                                                                                                    |
| python_startup_no_site     | 7.49 ms                                                                                                           | 9.93 ms: 1.33x slower                                                                                                   |
| coverage                   | 82.3 ms                                                                                                           | 111 ms: 1.35x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, coroutines

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.21x