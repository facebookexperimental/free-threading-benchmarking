# Results vs. base

- fork: python
- ref: f5dd52df16e1b3f3f8cc
- machine: linux-x86_64
- commit hash: f5dd52d
- commit date: 2026-09-11
- overall geometric mean: 1.108x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 261 ms                                                                                                          | 298 ms: 1.14x slower                                                                                                  |
| docutils       | 2.39 sec                                                                                                        | 2.95 sec: 1.23x slower                                                                                                |
| html5lib       | 60.0 ms                                                                                                         | 68.1 ms: 1.13x slower                                                                                                 |
| sphinx         | 1000 ms                                                                                                         | 1.11 sec: 1.11x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 760 ms                                                                                                          | 706 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 507 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 776 ms                                                                                                          | 728 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 587 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 25.9 ms: 1.09x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 565 ms                                                                                                          | 614 ms: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 405 ms: 1.11x slower                                                                                                  |
| async_tree_memoization     | 403 ms                                                                                                          | 454 ms: 1.13x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 338 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 329 ms                                                                                                          | 375 ms: 1.14x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 415 ms: 1.21x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 182 ms: 1.03x faster                                                                                                  |
| float          | 73.1 ms                                                                                                         | 85.1 ms: 1.16x slower                                                                                                 |
| nbody          | 92.4 ms                                                                                                         | 125 ms: 1.35x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                                                         | 20.9 ms: 1.04x faster                                                                                                 |
| regex_dna      | 186 ms                                                                                                          | 187 ms: 1.00x slower                                                                                                  |
| regex_effbot   | 2.89 ms                                                                                                         | 3.00 ms: 1.04x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 172 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.4 ms                                                                                                         | 96.6 ms: 1.06x slower                                                                                                 |
| json_dumps           | 9.36 ms                                                                                                         | 10.2 ms: 1.09x slower                                                                                                 |
| tomli_loads          | 1.80 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| pickle_pure_python   | 305 us                                                                                                          | 339 us: 1.11x slower                                                                                                  |
| json_loads           | 27.4 us                                                                                                         | 30.9 us: 1.13x slower                                                                                                 |
| unpickle_pure_python | 213 us                                                                                                          | 243 us: 1.14x slower                                                                                                  |
| xml_etree_generate   | 88.2 ms                                                                                                         | 101 ms: 1.14x slower                                                                                                  |
| xml_etree_process    | 62.4 ms                                                                                                         | 75.8 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 13.0 ms                                                                                                         | 16.6 ms: 1.28x slower                                                                                                 |
| python_startup_no_site | 7.74 ms                                                                                                         | 9.99 ms: 1.29x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                         | 42.9 ms: 1.17x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 16.1 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json | results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 265 ms                                                                                                          | 6.76 ms: 39.22x faster                                                                                                |
| gc_traversal               | 4.04 ms                                                                                                         | 1.80 ms: 2.25x faster                                                                                                 |
| create_gc_cycles           | 1.66 ms                                                                                                         | 1.38 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.31 us                                                                                                         | 1.97 us: 1.17x faster                                                                                                 |
| async_tree_io_tg           | 760 ms                                                                                                          | 706 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 507 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 776 ms                                                                                                          | 728 ms: 1.07x faster                                                                                                  |
| regex_v8                   | 21.8 ms                                                                                                         | 20.9 ms: 1.04x faster                                                                                                 |
| pidigits                   | 187 ms                                                                                                          | 182 ms: 1.03x faster                                                                                                  |
| regex_dna                  | 186 ms                                                                                                          | 187 ms: 1.00x slower                                                                                                  |
| pathlib                    | 17.7 ms                                                                                                         | 18.0 ms: 1.02x slower                                                                                                 |
| dulwich_log                | 67.9 ms                                                                                                         | 70.4 ms: 1.04x slower                                                                                                 |
| bpe_tokeniser              | 4.24 sec                                                                                                        | 4.40 sec: 1.04x slower                                                                                                |
| regex_effbot               | 2.89 ms                                                                                                         | 3.00 ms: 1.04x slower                                                                                                 |
| pycparser                  | 1.12 sec                                                                                                        | 1.17 sec: 1.04x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 587 ms: 1.05x slower                                                                                                  |
| xml_etree_iterparse        | 91.4 ms                                                                                                         | 96.6 ms: 1.06x slower                                                                                                 |
| k_core                     | 2.09 sec                                                                                                        | 2.26 sec: 1.08x slower                                                                                                |
| coroutines                 | 23.8 ms                                                                                                         | 25.9 ms: 1.09x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 565 ms                                                                                                          | 614 ms: 1.09x slower                                                                                                  |
| logging_silent             | 98.8 ns                                                                                                         | 108 ns: 1.09x slower                                                                                                  |
| json_dumps                 | 9.36 ms                                                                                                         | 10.2 ms: 1.09x slower                                                                                                 |
| tomli_loads                | 1.80 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| json                       | 4.91 ms                                                                                                         | 5.40 ms: 1.10x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.48 ms: 1.10x slower                                                                                                 |
| pprint_safe_repr           | 733 ms                                                                                                          | 810 ms: 1.11x slower                                                                                                  |
| sphinx                     | 1000 ms                                                                                                         | 1.11 sec: 1.11x slower                                                                                                |
| telco                      | 160 ms                                                                                                          | 178 ms: 1.11x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 405 ms: 1.11x slower                                                                                                  |
| scimark_fft                | 316 ms                                                                                                          | 351 ms: 1.11x slower                                                                                                  |
| pickle_pure_python         | 305 us                                                                                                          | 339 us: 1.11x slower                                                                                                  |
| scimark_sor                | 110 ms                                                                                                          | 123 ms: 1.11x slower                                                                                                  |
| sqlglot_v2_normalize       | 104 ms                                                                                                          | 116 ms: 1.12x slower                                                                                                  |
| scimark_lu                 | 119 ms                                                                                                          | 134 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_optimize        | 52.0 ms                                                                                                         | 58.2 ms: 1.12x slower                                                                                                 |
| deltablue                  | 3.37 ms                                                                                                         | 3.79 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 403 ms                                                                                                          | 454 ms: 1.13x slower                                                                                                  |
| pprint_pformat             | 1.49 sec                                                                                                        | 1.69 sec: 1.13x slower                                                                                                |
| sympy_expand               | 475 ms                                                                                                          | 537 ms: 1.13x slower                                                                                                  |
| json_loads                 | 27.4 us                                                                                                         | 30.9 us: 1.13x slower                                                                                                 |
| html5lib                   | 60.0 ms                                                                                                         | 68.1 ms: 1.13x slower                                                                                                 |
| comprehensions             | 16.1 us                                                                                                         | 18.3 us: 1.13x slower                                                                                                 |
| many_optionals             | 900 us                                                                                                          | 1.02 ms: 1.14x slower                                                                                                 |
| chaos                      | 54.3 ms                                                                                                         | 61.8 ms: 1.14x slower                                                                                                 |
| go                         | 106 ms                                                                                                          | 121 ms: 1.14x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 338 ms: 1.14x slower                                                                                                  |
| sympy_str                  | 279 ms                                                                                                          | 319 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 329 ms                                                                                                          | 375 ms: 1.14x slower                                                                                                  |
| 2to3                       | 261 ms                                                                                                          | 298 ms: 1.14x slower                                                                                                  |
| unpickle_pure_python       | 213 us                                                                                                          | 243 us: 1.14x slower                                                                                                  |
| xml_etree_generate         | 88.2 ms                                                                                                         | 101 ms: 1.14x slower                                                                                                  |
| sympy_integrate            | 19.3 ms                                                                                                         | 22.1 ms: 1.15x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 132 ms: 1.15x slower                                                                                                  |
| deepcopy                   | 236 us                                                                                                          | 272 us: 1.15x slower                                                                                                  |
| sympy_sum                  | 158 ms                                                                                                          | 182 ms: 1.15x slower                                                                                                  |
| spectral_norm              | 93.4 ms                                                                                                         | 108 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.32 sec: 1.16x slower                                                                                                |
| deepcopy_reduce            | 2.59 us                                                                                                         | 3.01 us: 1.16x slower                                                                                                 |
| generators                 | 29.5 ms                                                                                                         | 34.3 ms: 1.16x slower                                                                                                 |
| regex_compile              | 148 ms                                                                                                          | 172 ms: 1.16x slower                                                                                                  |
| subparsers                 | 9.04 ms                                                                                                         | 10.5 ms: 1.16x slower                                                                                                 |
| float                      | 73.1 ms                                                                                                         | 85.1 ms: 1.16x slower                                                                                                 |
| deepcopy_memo              | 26.8 us                                                                                                         | 31.3 us: 1.17x slower                                                                                                 |
| hexiom                     | 5.66 ms                                                                                                         | 6.63 ms: 1.17x slower                                                                                                 |
| django_template            | 36.6 ms                                                                                                         | 42.9 ms: 1.17x slower                                                                                                 |
| raytrace                   | 253 ms                                                                                                          | 298 ms: 1.18x slower                                                                                                  |
| richards                   | 44.8 ms                                                                                                         | 53.3 ms: 1.19x slower                                                                                                 |
| thrift                     | 779 us                                                                                                          | 927 us: 1.19x slower                                                                                                  |
| logging_simple             | 5.88 us                                                                                                         | 7.01 us: 1.19x slower                                                                                                 |
| richards_super             | 51.1 ms                                                                                                         | 61.1 ms: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.76 ms: 1.20x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.63 ms                                                                                                         | 5.59 ms: 1.21x slower                                                                                                 |
| logging_format             | 6.67 us                                                                                                         | 8.04 us: 1.21x slower                                                                                                 |
| pyflate                    | 386 ms                                                                                                          | 468 ms: 1.21x slower                                                                                                  |
| typing_runtime_protocols   | 121 us                                                                                                          | 147 us: 1.21x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 415 ms: 1.21x slower                                                                                                  |
| xml_etree_process          | 62.4 ms                                                                                                         | 75.8 ms: 1.22x slower                                                                                                 |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.43 ms: 1.23x slower                                                                                                 |
| nqueens                    | 73.5 ms                                                                                                         | 90.5 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.39 sec                                                                                                        | 2.95 sec: 1.23x slower                                                                                                |
| shortest_path              | 434 ms                                                                                                          | 536 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 371 ms                                                                                                          | 462 ms: 1.25x slower                                                                                                  |
| meteor_contest             | 102 ms                                                                                                          | 128 ms: 1.25x slower                                                                                                  |
| connected_components       | 394 ms                                                                                                          | 494 ms: 1.25x slower                                                                                                  |
| scimark_monte_carlo        | 63.0 ms                                                                                                         | 79.1 ms: 1.25x slower                                                                                                 |
| python_startup             | 13.0 ms                                                                                                         | 16.6 ms: 1.28x slower                                                                                                 |
| python_startup_no_site     | 7.74 ms                                                                                                         | 9.99 ms: 1.29x slower                                                                                                 |
| crypto_pyaes               | 67.4 ms                                                                                                         | 89.4 ms: 1.33x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 16.1 ms: 1.34x slower                                                                                                 |
| nbody                      | 92.4 ms                                                                                                         | 125 ms: 1.35x slower                                                                                                  |
| coverage                   | 83.4 ms                                                                                                         | 118 ms: 1.41x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.108x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x