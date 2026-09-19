# Results vs. base

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: linux-x86_64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 261 ms                                                                                                          | 296 ms: 1.13x slower                                                                                                  |
| docutils       | 2.41 sec                                                                                                        | 2.94 sec: 1.22x slower                                                                                                |
| html5lib       | 59.8 ms                                                                                                         | 65.9 ms: 1.10x slower                                                                                                 |
| sphinx         | 985 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 759 ms                                                                                                          | 705 ms: 1.08x faster                                                                                                  |
| async_tree_io              | 781 ms                                                                                                          | 728 ms: 1.07x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 508 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 551 ms                                                                                                          | 588 ms: 1.07x slower                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 25.6 ms: 1.09x slower                                                                                                 |
| async_tree_memoization_tg  | 370 ms                                                                                                          | 406 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 557 ms                                                                                                          | 614 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 406 ms                                                                                                          | 451 ms: 1.11x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 337 ms: 1.12x slower                                                                                                  |
| async_tree_none            | 332 ms                                                                                                          | 375 ms: 1.13x slower                                                                                                  |
| async_generators           | 345 ms                                                                                                          | 415 ms: 1.20x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                          | 180 ms: 1.08x faster                                                                                                  |
| float          | 72.6 ms                                                                                                         | 85.1 ms: 1.17x slower                                                                                                 |
| nbody          | 91.4 ms                                                                                                         | 122 ms: 1.34x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 20.9 ms                                                                                                         | 21.3 ms: 1.02x slower                                                                                                 |
| regex_dna      | 171 ms                                                                                                          | 183 ms: 1.07x slower                                                                                                  |
| regex_effbot   | 2.62 ms                                                                                                         | 3.00 ms: 1.14x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 145 ms                                                                                                          | 141 ms: 1.03x faster                                                                                                  |
| xml_etree_iterparse  | 92.1 ms                                                                                                         | 95.2 ms: 1.03x slower                                                                                                 |
| json_dumps           | 9.48 ms                                                                                                         | 9.99 ms: 1.05x slower                                                                                                 |
| pickle_pure_python   | 309 us                                                                                                          | 339 us: 1.09x slower                                                                                                  |
| tomli_loads          | 1.79 sec                                                                                                        | 1.96 sec: 1.10x slower                                                                                                |
| unpickle_pure_python | 216 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| xml_etree_generate   | 89.2 ms                                                                                                         | 99.0 ms: 1.11x slower                                                                                                 |
| json_loads           | 27.0 us                                                                                                         | 30.4 us: 1.12x slower                                                                                                 |
| xml_etree_process    | 63.5 ms                                                                                                         | 74.9 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.72 ms                                                                                                         | 9.73 ms: 1.26x slower                                                                                                 |
| python_startup         | 13.0 ms                                                                                                         | 16.4 ms: 1.26x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 37.0 ms                                                                                                         | 41.0 ms: 1.11x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 16.1 ms: 1.37x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json | results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 288 ms                                                                                                          | 6.73 ms: 42.80x faster                                                                                                |
| gc_traversal               | 3.71 ms                                                                                                         | 1.77 ms: 2.10x faster                                                                                                 |
| create_gc_cycles           | 1.63 ms                                                                                                         | 1.39 ms: 1.18x faster                                                                                                 |
| sqlite_synth               | 2.21 us                                                                                                         | 1.93 us: 1.14x faster                                                                                                 |
| pidigits                   | 195 ms                                                                                                          | 180 ms: 1.08x faster                                                                                                  |
| async_tree_io_tg           | 759 ms                                                                                                          | 705 ms: 1.08x faster                                                                                                  |
| async_tree_io              | 781 ms                                                                                                          | 728 ms: 1.07x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 508 ms: 1.07x faster                                                                                                  |
| xml_etree_parse            | 145 ms                                                                                                          | 141 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 20.9 ms                                                                                                         | 21.3 ms: 1.02x slower                                                                                                 |
| pathlib                    | 17.8 ms                                                                                                         | 18.2 ms: 1.02x slower                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                        | 1.17 sec: 1.03x slower                                                                                                |
| dulwich_log                | 67.6 ms                                                                                                         | 69.9 ms: 1.03x slower                                                                                                 |
| xml_etree_iterparse        | 92.1 ms                                                                                                         | 95.2 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.21 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| json_dumps                 | 9.48 ms                                                                                                         | 9.99 ms: 1.05x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 551 ms                                                                                                          | 588 ms: 1.07x slower                                                                                                  |
| regex_dna                  | 171 ms                                                                                                          | 183 ms: 1.07x slower                                                                                                  |
| json                       | 4.98 ms                                                                                                         | 5.35 ms: 1.07x slower                                                                                                 |
| k_core                     | 2.08 sec                                                                                                        | 2.24 sec: 1.08x slower                                                                                                |
| logging_silent             | 97.1 ns                                                                                                         | 105 ns: 1.08x slower                                                                                                  |
| scimark_lu                 | 120 ms                                                                                                          | 130 ms: 1.08x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 175 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 309 us                                                                                                          | 339 us: 1.09x slower                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 25.6 ms: 1.09x slower                                                                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                                                          | 116 ms: 1.09x slower                                                                                                  |
| tomli_loads                | 1.79 sec                                                                                                        | 1.96 sec: 1.10x slower                                                                                                |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.48 ms: 1.10x slower                                                                                                 |
| async_tree_memoization_tg  | 370 ms                                                                                                          | 406 ms: 1.10x slower                                                                                                  |
| html5lib                   | 59.8 ms                                                                                                         | 65.9 ms: 1.10x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 557 ms                                                                                                          | 614 ms: 1.10x slower                                                                                                  |
| scimark_fft                | 309 ms                                                                                                          | 341 ms: 1.10x slower                                                                                                  |
| deltablue                  | 3.35 ms                                                                                                         | 3.70 ms: 1.10x slower                                                                                                 |
| unpickle_pure_python       | 216 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| many_optionals             | 912 us                                                                                                          | 1.01 ms: 1.11x slower                                                                                                 |
| django_template            | 37.0 ms                                                                                                         | 41.0 ms: 1.11x slower                                                                                                 |
| xml_etree_generate         | 89.2 ms                                                                                                         | 99.0 ms: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 721 ms                                                                                                          | 801 ms: 1.11x slower                                                                                                  |
| async_tree_memoization     | 406 ms                                                                                                          | 451 ms: 1.11x slower                                                                                                  |
| chaos                      | 54.1 ms                                                                                                         | 60.6 ms: 1.12x slower                                                                                                 |
| async_tree_none_tg         | 301 ms                                                                                                          | 337 ms: 1.12x slower                                                                                                  |
| sympy_expand               | 476 ms                                                                                                          | 534 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.9 ms                                                                                                         | 58.3 ms: 1.12x slower                                                                                                 |
| json_loads                 | 27.0 us                                                                                                         | 30.4 us: 1.12x slower                                                                                                 |
| pprint_pformat             | 1.48 sec                                                                                                        | 1.67 sec: 1.13x slower                                                                                                |
| scimark_sor                | 108 ms                                                                                                          | 122 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 332 ms                                                                                                          | 375 ms: 1.13x slower                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 18.0 us: 1.13x slower                                                                                                 |
| sympy_sum                  | 159 ms                                                                                                          | 180 ms: 1.13x slower                                                                                                  |
| 2to3                       | 261 ms                                                                                                          | 296 ms: 1.13x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 120 ms: 1.14x slower                                                                                                  |
| sphinx                     | 985 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| subparsers                 | 9.09 ms                                                                                                         | 10.4 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.3 ms                                                                                                         | 22.0 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 279 ms                                                                                                          | 319 ms: 1.14x slower                                                                                                  |
| regex_effbot               | 2.62 ms                                                                                                         | 3.00 ms: 1.14x slower                                                                                                 |
| pyflate                    | 398 ms                                                                                                          | 456 ms: 1.15x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| generators                 | 29.6 ms                                                                                                         | 34.1 ms: 1.15x slower                                                                                                 |
| pylint                     | 112 ms                                                                                                          | 129 ms: 1.15x slower                                                                                                  |
| logging_simple             | 6.04 us                                                                                                         | 6.98 us: 1.15x slower                                                                                                 |
| deepcopy_reduce            | 2.53 us                                                                                                         | 2.92 us: 1.16x slower                                                                                                 |
| hexiom                     | 5.64 ms                                                                                                         | 6.54 ms: 1.16x slower                                                                                                 |
| mdp                        | 1.12 sec                                                                                                        | 1.31 sec: 1.16x slower                                                                                                |
| deepcopy                   | 228 us                                                                                                          | 267 us: 1.17x slower                                                                                                  |
| float                      | 72.6 ms                                                                                                         | 85.1 ms: 1.17x slower                                                                                                 |
| raytrace                   | 249 ms                                                                                                          | 292 ms: 1.17x slower                                                                                                  |
| thrift                     | 789 us                                                                                                          | 930 us: 1.18x slower                                                                                                  |
| xml_etree_process          | 63.5 ms                                                                                                         | 74.9 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.74 ms: 1.18x slower                                                                                                 |
| logging_format             | 6.77 us                                                                                                         | 8.00 us: 1.18x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.41 ms                                                                                                         | 5.21 ms: 1.18x slower                                                                                                 |
| richards_super             | 51.1 ms                                                                                                         | 60.6 ms: 1.19x slower                                                                                                 |
| richards                   | 44.5 ms                                                                                                         | 53.0 ms: 1.19x slower                                                                                                 |
| deepcopy_memo              | 27.5 us                                                                                                         | 33.0 us: 1.20x slower                                                                                                 |
| async_generators           | 345 ms                                                                                                          | 415 ms: 1.20x slower                                                                                                  |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.41 ms: 1.21x slower                                                                                                 |
| scimark_monte_carlo        | 63.9 ms                                                                                                         | 77.1 ms: 1.21x slower                                                                                                 |
| shortest_path              | 441 ms                                                                                                          | 533 ms: 1.21x slower                                                                                                  |
| docutils                   | 2.41 sec                                                                                                        | 2.94 sec: 1.22x slower                                                                                                |
| nqueens                    | 72.9 ms                                                                                                         | 89.5 ms: 1.23x slower                                                                                                 |
| connected_components       | 395 ms                                                                                                          | 486 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 119 us                                                                                                          | 147 us: 1.24x slower                                                                                                  |
| spectral_norm              | 86.3 ms                                                                                                         | 107 ms: 1.24x slower                                                                                                  |
| meteor_contest             | 100 ms                                                                                                          | 125 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 372 ms                                                                                                          | 467 ms: 1.26x slower                                                                                                  |
| python_startup_no_site     | 7.72 ms                                                                                                         | 9.73 ms: 1.26x slower                                                                                                 |
| python_startup             | 13.0 ms                                                                                                         | 16.4 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 66.9 ms                                                                                                         | 88.2 ms: 1.32x slower                                                                                                 |
| nbody                      | 91.4 ms                                                                                                         | 122 ms: 1.34x slower                                                                                                  |
| mako                       | 11.8 ms                                                                                                         | 16.1 ms: 1.37x slower                                                                                                 |
| coverage                   | 84.7 ms                                                                                                         | 118 ms: 1.39x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.18x