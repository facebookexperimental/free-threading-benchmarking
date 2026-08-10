# Results vs. base

- fork: python
- ref: 87b120fdb58afd8f7cb7
- machine: linux-x86_64
- commit hash: 87b120f
- commit date: 2026-08-09
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 261 ms                                                                                                          | 298 ms: 1.14x slower                                                                                                  |
| docutils       | 2.37 sec                                                                                                        | 2.93 sec: 1.24x slower                                                                                                |
| html5lib       | 57.7 ms                                                                                                         | 67.2 ms: 1.17x slower                                                                                                 |
| sphinx         | 988 ms                                                                                                          | 1.12 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 763 ms                                                                                                          | 678 ms: 1.13x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 722 ms                                                                                                          | 696 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 554 ms                                                                                                          | 575 ms: 1.04x slower                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 24.2 ms: 1.06x slower                                                                                                 |
| async_tree_none_tg         | 297 ms                                                                                                          | 321 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 363 ms                                                                                                          | 393 ms: 1.08x slower                                                                                                  |
| async_tree_memoization     | 373 ms                                                                                                          | 419 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 534 ms                                                                                                          | 602 ms: 1.13x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 387 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 342 ms: 1.18x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 188 ms                                                                                                          | 181 ms: 1.04x faster                                                                                                  |
| float          | 72.8 ms                                                                                                         | 84.2 ms: 1.16x slower                                                                                                 |
| nbody          | 92.6 ms                                                                                                         | 120 ms: 1.30x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.1 ms                                                                                                         | 20.5 ms: 1.03x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 183 ms: 1.04x slower                                                                                                  |
| regex_compile  | 148 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| regex_effbot   | 2.56 ms                                                                                                         | 3.01 ms: 1.18x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 91.7 ms                                                                                                         | 95.0 ms: 1.04x slower                                                                                                 |
| json_dumps           | 9.94 ms                                                                                                         | 10.7 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| tomli_loads          | 1.79 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| unpickle_pure_python | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| json_loads           | 27.7 us                                                                                                         | 30.7 us: 1.11x slower                                                                                                 |
| xml_etree_generate   | 87.5 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| xml_etree_process    | 62.3 ms                                                                                                         | 74.7 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.08 ms                                                                                                         | 9.26 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.5 ms                                                                                                         | 41.4 ms: 1.14x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.7 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json | results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 227 ms                                                                                                          | 13.2 ms: 17.13x faster                                                                                                |
| gc_traversal               | 3.54 ms                                                                                                         | 1.77 ms: 2.00x faster                                                                                                 |
| create_gc_cycles           | 1.64 ms                                                                                                         | 1.39 ms: 1.18x faster                                                                                                 |
| sqlite_synth               | 2.23 us                                                                                                         | 1.92 us: 1.16x faster                                                                                                 |
| async_tree_io_tg           | 763 ms                                                                                                          | 678 ms: 1.13x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| pidigits                   | 188 ms                                                                                                          | 181 ms: 1.04x faster                                                                                                  |
| async_tree_io              | 722 ms                                                                                                          | 696 ms: 1.04x faster                                                                                                  |
| regex_v8                   | 21.1 ms                                                                                                         | 20.5 ms: 1.03x faster                                                                                                 |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| bpe_tokeniser              | 4.23 sec                                                                                                        | 4.36 sec: 1.03x slower                                                                                                |
| xml_etree_iterparse        | 91.7 ms                                                                                                         | 95.0 ms: 1.04x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 554 ms                                                                                                          | 575 ms: 1.04x slower                                                                                                  |
| dulwich_log                | 67.0 ms                                                                                                         | 69.5 ms: 1.04x slower                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                        | 1.17 sec: 1.04x slower                                                                                                |
| regex_dna                  | 176 ms                                                                                                          | 183 ms: 1.04x slower                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 24.2 ms: 1.06x slower                                                                                                 |
| logging_silent             | 99.4 ns                                                                                                         | 106 ns: 1.06x slower                                                                                                  |
| json_dumps                 | 9.94 ms                                                                                                         | 10.7 ms: 1.08x slower                                                                                                 |
| async_tree_none_tg         | 297 ms                                                                                                          | 321 ms: 1.08x slower                                                                                                  |
| k_core                     | 2.09 sec                                                                                                        | 2.26 sec: 1.08x slower                                                                                                |
| deltablue                  | 3.40 ms                                                                                                         | 3.68 ms: 1.08x slower                                                                                                 |
| async_tree_memoization_tg  | 363 ms                                                                                                          | 393 ms: 1.08x slower                                                                                                  |
| pickle_pure_python         | 306 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| scimark_fft                | 309 ms                                                                                                          | 338 ms: 1.09x slower                                                                                                  |
| bench_thread_pool          | 1.36 ms                                                                                                         | 1.49 ms: 1.10x slower                                                                                                 |
| telco                      | 159 ms                                                                                                          | 175 ms: 1.10x slower                                                                                                  |
| scimark_sor                | 111 ms                                                                                                          | 122 ms: 1.10x slower                                                                                                  |
| tomli_loads                | 1.79 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| json                       | 4.88 ms                                                                                                         | 5.39 ms: 1.10x slower                                                                                                 |
| unpickle_pure_python       | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| many_optionals             | 915 us                                                                                                          | 1.02 ms: 1.11x slower                                                                                                 |
| json_loads                 | 27.7 us                                                                                                         | 30.7 us: 1.11x slower                                                                                                 |
| scimark_lu                 | 116 ms                                                                                                          | 130 ms: 1.11x slower                                                                                                  |
| sympy_expand               | 473 ms                                                                                                          | 531 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.7 ms                                                                                                         | 58.1 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 373 ms                                                                                                          | 419 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 534 ms                                                                                                          | 602 ms: 1.13x slower                                                                                                  |
| sphinx                     | 988 ms                                                                                                          | 1.12 sec: 1.13x slower                                                                                                |
| deepcopy_reduce            | 2.58 us                                                                                                         | 2.92 us: 1.13x slower                                                                                                 |
| sqlglot_v2_normalize       | 102 ms                                                                                                          | 115 ms: 1.13x slower                                                                                                  |
| pprint_safe_repr           | 730 ms                                                                                                          | 826 ms: 1.13x slower                                                                                                  |
| comprehensions             | 15.8 us                                                                                                         | 17.9 us: 1.13x slower                                                                                                 |
| chaos                      | 53.7 ms                                                                                                         | 60.8 ms: 1.13x slower                                                                                                 |
| sympy_str                  | 279 ms                                                                                                          | 316 ms: 1.13x slower                                                                                                  |
| hexiom                     | 5.72 ms                                                                                                         | 6.49 ms: 1.13x slower                                                                                                 |
| async_generators           | 341 ms                                                                                                          | 387 ms: 1.14x slower                                                                                                  |
| django_template            | 36.5 ms                                                                                                         | 41.4 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.7 ms: 1.14x slower                                                                                                 |
| sympy_sum                  | 158 ms                                                                                                          | 180 ms: 1.14x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| 2to3                       | 261 ms                                                                                                          | 298 ms: 1.14x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| xml_etree_generate         | 87.5 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| raytrace                   | 255 ms                                                                                                          | 294 ms: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.48 sec                                                                                                        | 1.71 sec: 1.16x slower                                                                                                |
| float                      | 72.8 ms                                                                                                         | 84.2 ms: 1.16x slower                                                                                                 |
| subparsers                 | 9.03 ms                                                                                                         | 10.4 ms: 1.16x slower                                                                                                 |
| spectral_norm              | 90.9 ms                                                                                                         | 105 ms: 1.16x slower                                                                                                  |
| logging_simple             | 6.05 us                                                                                                         | 7.02 us: 1.16x slower                                                                                                 |
| mdp                        | 1.12 sec                                                                                                        | 1.31 sec: 1.16x slower                                                                                                |
| scimark_sparse_mat_mult    | 4.58 ms                                                                                                         | 5.33 ms: 1.17x slower                                                                                                 |
| html5lib                   | 57.7 ms                                                                                                         | 67.2 ms: 1.17x slower                                                                                                 |
| deepcopy                   | 233 us                                                                                                          | 271 us: 1.17x slower                                                                                                  |
| thrift                     | 787 us                                                                                                          | 924 us: 1.17x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 342 ms: 1.18x slower                                                                                                  |
| regex_effbot               | 2.56 ms                                                                                                         | 3.01 ms: 1.18x slower                                                                                                 |
| generators                 | 27.9 ms                                                                                                         | 33.0 ms: 1.18x slower                                                                                                 |
| richards_super             | 50.9 ms                                                                                                         | 60.5 ms: 1.19x slower                                                                                                 |
| richards                   | 44.4 ms                                                                                                         | 52.9 ms: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.74 ms: 1.19x slower                                                                                                 |
| xml_etree_process          | 62.3 ms                                                                                                         | 74.7 ms: 1.20x slower                                                                                                 |
| pyflate                    | 388 ms                                                                                                          | 465 ms: 1.20x slower                                                                                                  |
| deepcopy_memo              | 26.6 us                                                                                                         | 32.0 us: 1.21x slower                                                                                                 |
| nqueens                    | 73.1 ms                                                                                                         | 88.3 ms: 1.21x slower                                                                                                 |
| logging_format             | 6.76 us                                                                                                         | 8.20 us: 1.21x slower                                                                                                 |
| shortest_path              | 439 ms                                                                                                          | 535 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.42 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 119 us                                                                                                          | 145 us: 1.22x slower                                                                                                  |
| connected_components       | 399 ms                                                                                                          | 492 ms: 1.24x slower                                                                                                  |
| docutils                   | 2.37 sec                                                                                                        | 2.93 sec: 1.24x slower                                                                                                |
| scimark_monte_carlo        | 62.9 ms                                                                                                         | 78.0 ms: 1.24x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 102 ms                                                                                                          | 128 ms: 1.25x slower                                                                                                  |
| fannkuch                   | 370 ms                                                                                                          | 468 ms: 1.26x slower                                                                                                  |
| nbody                      | 92.6 ms                                                                                                         | 120 ms: 1.30x slower                                                                                                  |
| python_startup_no_site     | 7.08 ms                                                                                                         | 9.26 ms: 1.31x slower                                                                                                 |
| crypto_pyaes               | 67.3 ms                                                                                                         | 89.2 ms: 1.33x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.7 ms: 1.33x slower                                                                                                 |
| coverage                   | 83.4 ms                                                                                                         | 114 ms: 1.36x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x