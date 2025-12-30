# Results vs. base

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: linux-x86_64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.103x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                                                            | 275 ms: 1.12x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 2.73 sec: 1.07x slower                                                                                                  |
| html5lib       | 59.7 ms                                                                                                           | 65.9 ms: 1.10x slower                                                                                                   |
| sphinx         | 965 ms                                                                                                            | 1.06 sec: 1.09x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 542 ms                                                                                                            | 511 ms: 1.06x faster                                                                                                    |
| coroutines                 | 23.4 ms                                                                                                           | 24.2 ms: 1.03x slower                                                                                                   |
| async_tree_io_tg           | 582 ms                                                                                                            | 612 ms: 1.05x slower                                                                                                    |
| async_tree_memoization_tg  | 307 ms                                                                                                            | 323 ms: 1.05x slower                                                                                                    |
| async_tree_none_tg         | 245 ms                                                                                                            | 262 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 523 ms: 1.08x slower                                                                                                    |
| async_generators           | 342 ms                                                                                                            | 377 ms: 1.10x slower                                                                                                    |
| async_tree_io              | 542 ms                                                                                                            | 614 ms: 1.13x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 482 ms                                                                                                            | 550 ms: 1.14x slower                                                                                                    |
| async_tree_memoization     | 305 ms                                                                                                            | 351 ms: 1.15x slower                                                                                                    |
| async_tree_none            | 240 ms                                                                                                            | 286 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 201 ms                                                                                                            | 192 ms: 1.05x faster                                                                                                    |
| float          | 71.7 ms                                                                                                           | 73.2 ms: 1.02x slower                                                                                                   |
| nbody          | 91.8 ms                                                                                                           | 125 ms: 1.37x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                                                           | 21.4 ms: 1.06x faster                                                                                                   |
| regex_dna      | 175 ms                                                                                                            | 174 ms: 1.01x faster                                                                                                    |
| regex_effbot   | 2.81 ms                                                                                                           | 2.88 ms: 1.03x slower                                                                                                   |
| regex_compile  | 123 ms                                                                                                            | 141 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.8 ms                                                                                                           | 88.3 ms: 1.04x slower                                                                                                   |
| pickle_pure_python   | 309 us                                                                                                            | 333 us: 1.08x slower                                                                                                    |
| tomli_loads          | 2.06 sec                                                                                                          | 2.27 sec: 1.10x slower                                                                                                  |
| unpickle_pure_python | 212 us                                                                                                            | 236 us: 1.11x slower                                                                                                    |
| json_dumps           | 10.0 ms                                                                                                           | 11.2 ms: 1.12x slower                                                                                                   |
| json_loads           | 28.4 us                                                                                                           | 32.3 us: 1.14x slower                                                                                                   |
| xml_etree_generate   | 82.6 ms                                                                                                           | 97.0 ms: 1.17x slower                                                                                                   |
| xml_etree_process    | 57.5 ms                                                                                                           | 69.6 ms: 1.21x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.7 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.28 ms                                                                                                           | 9.61 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                                                           | 40.6 ms: 1.14x slower                                                                                                   |
| genshi_xml      | 49.0 ms                                                                                                           | 57.7 ms: 1.18x slower                                                                                                   |
| genshi_text     | 21.2 ms                                                                                                           | 26.8 ms: 1.26x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 15.3 ms: 1.27x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.21x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json | results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 312 ms                                                                                                            | 7.11 ms: 43.94x faster                                                                                                  |
| gc_traversal               | 4.66 ms                                                                                                           | 1.87 ms: 2.49x faster                                                                                                   |
| create_gc_cycles           | 1.89 ms                                                                                                           | 1.50 ms: 1.26x faster                                                                                                   |
| sqlite_synth               | 2.31 us                                                                                                           | 2.06 us: 1.12x faster                                                                                                   |
| asyncio_websockets         | 542 ms                                                                                                            | 511 ms: 1.06x faster                                                                                                    |
| regex_v8                   | 22.6 ms                                                                                                           | 21.4 ms: 1.06x faster                                                                                                   |
| pidigits                   | 201 ms                                                                                                            | 192 ms: 1.05x faster                                                                                                    |
| regex_dna                  | 175 ms                                                                                                            | 174 ms: 1.01x faster                                                                                                    |
| float                      | 71.7 ms                                                                                                           | 73.2 ms: 1.02x slower                                                                                                   |
| pathlib                    | 17.5 ms                                                                                                           | 18.0 ms: 1.02x slower                                                                                                   |
| regex_effbot               | 2.81 ms                                                                                                           | 2.88 ms: 1.03x slower                                                                                                   |
| logging_silent             | 99.7 ns                                                                                                           | 103 ns: 1.03x slower                                                                                                    |
| coroutines                 | 23.4 ms                                                                                                           | 24.2 ms: 1.03x slower                                                                                                   |
| xml_etree_iterparse        | 84.8 ms                                                                                                           | 88.3 ms: 1.04x slower                                                                                                   |
| bpe_tokeniser              | 4.20 sec                                                                                                          | 4.38 sec: 1.04x slower                                                                                                  |
| async_tree_io_tg           | 582 ms                                                                                                            | 612 ms: 1.05x slower                                                                                                    |
| async_tree_memoization_tg  | 307 ms                                                                                                            | 323 ms: 1.05x slower                                                                                                    |
| pycparser                  | 1.08 sec                                                                                                          | 1.14 sec: 1.06x slower                                                                                                  |
| pylint                     | 285 ms                                                                                                            | 302 ms: 1.06x slower                                                                                                    |
| dulwich_log                | 66.6 ms                                                                                                           | 70.7 ms: 1.06x slower                                                                                                   |
| docutils                   | 2.55 sec                                                                                                          | 2.73 sec: 1.07x slower                                                                                                  |
| async_tree_none_tg         | 245 ms                                                                                                            | 262 ms: 1.07x slower                                                                                                    |
| pickle_pure_python         | 309 us                                                                                                            | 333 us: 1.08x slower                                                                                                    |
| many_optionals             | 955 us                                                                                                            | 1.03 ms: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 523 ms: 1.08x slower                                                                                                    |
| deltablue                  | 3.34 ms                                                                                                           | 3.62 ms: 1.09x slower                                                                                                   |
| json                       | 5.06 ms                                                                                                           | 5.51 ms: 1.09x slower                                                                                                   |
| sympy_expand               | 475 ms                                                                                                            | 519 ms: 1.09x slower                                                                                                    |
| sphinx                     | 965 ms                                                                                                            | 1.06 sec: 1.09x slower                                                                                                  |
| telco                      | 160 ms                                                                                                            | 175 ms: 1.10x slower                                                                                                    |
| tomli_loads                | 2.06 sec                                                                                                          | 2.27 sec: 1.10x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                            | 377 ms: 1.10x slower                                                                                                    |
| html5lib                   | 59.7 ms                                                                                                           | 65.9 ms: 1.10x slower                                                                                                   |
| comprehensions             | 16.0 us                                                                                                           | 17.7 us: 1.10x slower                                                                                                   |
| pprint_safe_repr           | 689 ms                                                                                                            | 763 ms: 1.11x slower                                                                                                    |
| unpickle_pure_python       | 212 us                                                                                                            | 236 us: 1.11x slower                                                                                                    |
| chaos                      | 56.3 ms                                                                                                           | 62.8 ms: 1.12x slower                                                                                                   |
| 2to3                       | 247 ms                                                                                                            | 275 ms: 1.12x slower                                                                                                    |
| json_dumps                 | 10.0 ms                                                                                                           | 11.2 ms: 1.12x slower                                                                                                   |
| deepcopy_reduce            | 2.62 us                                                                                                           | 2.94 us: 1.12x slower                                                                                                   |
| pprint_pformat             | 1.41 sec                                                                                                          | 1.58 sec: 1.12x slower                                                                                                  |
| hexiom                     | 5.69 ms                                                                                                           | 6.40 ms: 1.12x slower                                                                                                   |
| bench_thread_pool          | 1.30 ms                                                                                                           | 1.47 ms: 1.13x slower                                                                                                   |
| pyflate                    | 414 ms                                                                                                            | 468 ms: 1.13x slower                                                                                                    |
| deepcopy                   | 245 us                                                                                                            | 276 us: 1.13x slower                                                                                                    |
| subparsers                 | 9.08 ms                                                                                                           | 10.3 ms: 1.13x slower                                                                                                   |
| async_tree_io              | 542 ms                                                                                                            | 614 ms: 1.13x slower                                                                                                    |
| nqueens                    | 78.8 ms                                                                                                           | 89.4 ms: 1.13x slower                                                                                                   |
| json_loads                 | 28.4 us                                                                                                           | 32.3 us: 1.14x slower                                                                                                   |
| go                         | 105 ms                                                                                                            | 120 ms: 1.14x slower                                                                                                    |
| django_template            | 35.7 ms                                                                                                           | 40.6 ms: 1.14x slower                                                                                                   |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| deepcopy_memo              | 26.3 us                                                                                                           | 30.0 us: 1.14x slower                                                                                                   |
| regex_compile              | 123 ms                                                                                                            | 141 ms: 1.14x slower                                                                                                    |
| sympy_str                  | 272 ms                                                                                                            | 311 ms: 1.14x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 482 ms                                                                                                            | 550 ms: 1.14x slower                                                                                                    |
| scimark_fft                | 302 ms                                                                                                            | 345 ms: 1.14x slower                                                                                                    |
| generators                 | 28.0 ms                                                                                                           | 32.2 ms: 1.15x slower                                                                                                   |
| sympy_sum                  | 153 ms                                                                                                            | 177 ms: 1.15x slower                                                                                                    |
| async_tree_memoization     | 305 ms                                                                                                            | 351 ms: 1.15x slower                                                                                                    |
| scimark_sor                | 106 ms                                                                                                            | 122 ms: 1.15x slower                                                                                                    |
| sympy_integrate            | 18.9 ms                                                                                                           | 21.8 ms: 1.16x slower                                                                                                   |
| raytrace                   | 257 ms                                                                                                            | 298 ms: 1.16x slower                                                                                                    |
| sqlglot_v2_optimize        | 50.9 ms                                                                                                           | 59.7 ms: 1.17x slower                                                                                                   |
| thrift                     | 749 us                                                                                                            | 878 us: 1.17x slower                                                                                                    |
| xml_etree_generate         | 82.6 ms                                                                                                           | 97.0 ms: 1.17x slower                                                                                                   |
| genshi_xml                 | 49.0 ms                                                                                                           | 57.7 ms: 1.18x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                           | 1.77 ms: 1.18x slower                                                                                                   |
| fannkuch                   | 387 ms                                                                                                            | 457 ms: 1.18x slower                                                                                                    |
| k_core                     | 1.86 sec                                                                                                          | 2.20 sec: 1.18x slower                                                                                                  |
| logging_format             | 6.66 us                                                                                                           | 7.90 us: 1.19x slower                                                                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                                                            | 122 ms: 1.19x slower                                                                                                    |
| logging_simple             | 5.85 us                                                                                                           | 6.98 us: 1.19x slower                                                                                                   |
| async_tree_none            | 240 ms                                                                                                            | 286 ms: 1.19x slower                                                                                                    |
| sqlglot_v2_parse           | 1.20 ms                                                                                                           | 1.44 ms: 1.20x slower                                                                                                   |
| spectral_norm              | 92.0 ms                                                                                                           | 110 ms: 1.20x slower                                                                                                    |
| meteor_contest             | 102 ms                                                                                                            | 123 ms: 1.21x slower                                                                                                    |
| xml_etree_process          | 57.5 ms                                                                                                           | 69.6 ms: 1.21x slower                                                                                                   |
| richards                   | 42.1 ms                                                                                                           | 51.3 ms: 1.22x slower                                                                                                   |
| richards_super             | 48.2 ms                                                                                                           | 58.9 ms: 1.22x slower                                                                                                   |
| shortest_path              | 429 ms                                                                                                            | 529 ms: 1.23x slower                                                                                                    |
| scimark_lu                 | 105 ms                                                                                                            | 130 ms: 1.24x slower                                                                                                    |
| typing_runtime_protocols   | 154 us                                                                                                            | 192 us: 1.25x slower                                                                                                    |
| connected_components       | 386 ms                                                                                                            | 481 ms: 1.25x slower                                                                                                    |
| crypto_pyaes               | 69.2 ms                                                                                                           | 86.7 ms: 1.25x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.34 ms                                                                                                           | 5.45 ms: 1.26x slower                                                                                                   |
| genshi_text                | 21.2 ms                                                                                                           | 26.8 ms: 1.26x slower                                                                                                   |
| python_startup             | 12.4 ms                                                                                                           | 15.7 ms: 1.27x slower                                                                                                   |
| mako                       | 12.1 ms                                                                                                           | 15.3 ms: 1.27x slower                                                                                                   |
| scimark_monte_carlo        | 62.0 ms                                                                                                           | 78.8 ms: 1.27x slower                                                                                                   |
| python_startup_no_site     | 7.28 ms                                                                                                           | 9.61 ms: 1.32x slower                                                                                                   |
| nbody                      | 91.8 ms                                                                                                           | 125 ms: 1.37x slower                                                                                                    |
| coverage                   | 80.7 ms                                                                                                           | 113 ms: 1.40x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.103x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x