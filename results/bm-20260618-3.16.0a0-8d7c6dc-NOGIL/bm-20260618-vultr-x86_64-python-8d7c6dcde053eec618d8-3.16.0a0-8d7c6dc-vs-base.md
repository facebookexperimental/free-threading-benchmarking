# Results vs. base

- fork: python
- ref: 8d7c6dcde053eec618d8
- machine: linux-x86_64
- commit hash: 8d7c6dc
- commit date: 2026-06-18
- overall geometric mean: 1.102x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                                                          | 295 ms: 1.15x slower                                                                                                  |
| docutils       | 2.39 sec                                                                                                        | 2.94 sec: 1.23x slower                                                                                                |
| html5lib       | 58.9 ms                                                                                                         | 68.8 ms: 1.17x slower                                                                                                 |
| sphinx         | 978 ms                                                                                                          | 1.10 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 758 ms                                                                                                          | 679 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 701 ms: 1.03x faster                                                                                                  |
| async_tree_memoization_tg  | 369 ms                                                                                                          | 388 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.5 ms: 1.06x slower                                                                                                 |
| async_tree_none_tg         | 297 ms                                                                                                          | 320 ms: 1.08x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 605 ms: 1.08x slower                                                                                                  |
| async_tree_memoization     | 380 ms                                                                                                          | 415 ms: 1.09x slower                                                                                                  |
| async_generators           | 339 ms                                                                                                          | 391 ms: 1.15x slower                                                                                                  |
| async_tree_none            | 292 ms                                                                                                          | 339 ms: 1.16x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 540 ms                                                                                                          | 633 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 198 ms: 1.06x slower                                                                                                  |
| float          | 74.7 ms                                                                                                         | 86.1 ms: 1.15x slower                                                                                                 |
| nbody          | 94.3 ms                                                                                                         | 124 ms: 1.31x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                                                         | 20.1 ms: 1.10x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 177 ms: 1.00x slower                                                                                                  |
| regex_effbot   | 2.75 ms                                                                                                         | 2.97 ms: 1.08x slower                                                                                                 |
| regex_compile  | 122 ms                                                                                                          | 141 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 89.7 ms                                                                                                         | 94.0 ms: 1.05x slower                                                                                                 |
| tomli_loads          | 1.84 sec                                                                                                        | 1.96 sec: 1.07x slower                                                                                                |
| json_dumps           | 9.80 ms                                                                                                         | 10.5 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 311 us                                                                                                          | 338 us: 1.09x slower                                                                                                  |
| json_loads           | 27.4 us                                                                                                         | 30.0 us: 1.09x slower                                                                                                 |
| unpickle_pure_python | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| xml_etree_generate   | 86.0 ms                                                                                                         | 101 ms: 1.18x slower                                                                                                  |
| xml_etree_process    | 60.8 ms                                                                                                         | 75.0 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 6.94 ms                                                                                                         | 9.17 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.4 ms                                                                                                         | 40.1 ms: 1.13x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 16.1 ms: 1.36x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json | results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 253 ms                                                                                                          | 6.79 ms: 37.25x faster                                                                                                |
| gc_traversal               | 4.02 ms                                                                                                         | 1.77 ms: 2.27x faster                                                                                                 |
| create_gc_cycles           | 1.66 ms                                                                                                         | 1.38 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.27 us                                                                                                         | 1.93 us: 1.18x faster                                                                                                 |
| async_tree_io_tg           | 758 ms                                                                                                          | 679 ms: 1.12x faster                                                                                                  |
| regex_v8                   | 22.2 ms                                                                                                         | 20.1 ms: 1.10x faster                                                                                                 |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 701 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 176 ms                                                                                                          | 177 ms: 1.00x slower                                                                                                  |
| dulwich_log                | 68.1 ms                                                                                                         | 70.2 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.12 sec                                                                                                        | 1.16 sec: 1.04x slower                                                                                                |
| json                       | 5.07 ms                                                                                                         | 5.25 ms: 1.04x slower                                                                                                 |
| xml_etree_iterparse        | 89.7 ms                                                                                                         | 94.0 ms: 1.05x slower                                                                                                 |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| async_tree_memoization_tg  | 369 ms                                                                                                          | 388 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.5 ms: 1.06x slower                                                                                                 |
| pidigits                   | 187 ms                                                                                                          | 198 ms: 1.06x slower                                                                                                  |
| logging_silent             | 98.2 ns                                                                                                         | 104 ns: 1.06x slower                                                                                                  |
| tomli_loads                | 1.84 sec                                                                                                        | 1.96 sec: 1.07x slower                                                                                                |
| scimark_fft                | 324 ms                                                                                                          | 348 ms: 1.07x slower                                                                                                  |
| json_dumps                 | 9.80 ms                                                                                                         | 10.5 ms: 1.08x slower                                                                                                 |
| async_tree_none_tg         | 297 ms                                                                                                          | 320 ms: 1.08x slower                                                                                                  |
| regex_effbot               | 2.75 ms                                                                                                         | 2.97 ms: 1.08x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 605 ms: 1.08x slower                                                                                                  |
| pickle_pure_python         | 311 us                                                                                                          | 338 us: 1.09x slower                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 17.3 us: 1.09x slower                                                                                                 |
| async_tree_memoization     | 380 ms                                                                                                          | 415 ms: 1.09x slower                                                                                                  |
| deltablue                  | 3.35 ms                                                                                                         | 3.66 ms: 1.09x slower                                                                                                 |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.47 ms: 1.09x slower                                                                                                 |
| json_loads                 | 27.4 us                                                                                                         | 30.0 us: 1.09x slower                                                                                                 |
| many_optionals             | 917 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| scimark_sor                | 110 ms                                                                                                          | 121 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.05 sec                                                                                                        | 2.26 sec: 1.10x slower                                                                                                |
| telco                      | 159 ms                                                                                                          | 177 ms: 1.11x slower                                                                                                  |
| unpickle_pure_python       | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| pyflate                    | 411 ms                                                                                                          | 459 ms: 1.12x slower                                                                                                  |
| spectral_norm              | 95.2 ms                                                                                                         | 107 ms: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 724 ms                                                                                                          | 813 ms: 1.12x slower                                                                                                  |
| logging_format             | 6.87 us                                                                                                         | 7.72 us: 1.12x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.1 ms                                                                                                         | 57.6 ms: 1.13x slower                                                                                                 |
| sphinx                     | 978 ms                                                                                                          | 1.10 sec: 1.13x slower                                                                                                |
| scimark_lu                 | 114 ms                                                                                                          | 129 ms: 1.13x slower                                                                                                  |
| django_template            | 35.4 ms                                                                                                         | 40.1 ms: 1.13x slower                                                                                                 |
| subparsers                 | 9.33 ms                                                                                                         | 10.6 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| chaos                      | 54.9 ms                                                                                                         | 62.8 ms: 1.14x slower                                                                                                 |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| sympy_expand               | 457 ms                                                                                                          | 524 ms: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.47 sec                                                                                                        | 1.69 sec: 1.15x slower                                                                                                |
| logging_simple             | 5.98 us                                                                                                         | 6.86 us: 1.15x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.59 ms                                                                                                         | 5.27 ms: 1.15x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 132 ms: 1.15x slower                                                                                                  |
| async_generators           | 339 ms                                                                                                          | 391 ms: 1.15x slower                                                                                                  |
| hexiom                     | 5.75 ms                                                                                                         | 6.62 ms: 1.15x slower                                                                                                 |
| 2to3                       | 256 ms                                                                                                          | 295 ms: 1.15x slower                                                                                                  |
| regex_compile              | 122 ms                                                                                                          | 141 ms: 1.15x slower                                                                                                  |
| float                      | 74.7 ms                                                                                                         | 86.1 ms: 1.15x slower                                                                                                 |
| deepcopy                   | 234 us                                                                                                          | 270 us: 1.16x slower                                                                                                  |
| sympy_str                  | 273 ms                                                                                                          | 315 ms: 1.16x slower                                                                                                  |
| deepcopy_reduce            | 2.56 us                                                                                                         | 2.96 us: 1.16x slower                                                                                                 |
| mdp                        | 1.13 sec                                                                                                        | 1.31 sec: 1.16x slower                                                                                                |
| async_tree_none            | 292 ms                                                                                                          | 339 ms: 1.16x slower                                                                                                  |
| sympy_sum                  | 155 ms                                                                                                          | 180 ms: 1.16x slower                                                                                                  |
| sympy_integrate            | 18.9 ms                                                                                                         | 22.0 ms: 1.17x slower                                                                                                 |
| html5lib                   | 58.9 ms                                                                                                         | 68.8 ms: 1.17x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 540 ms                                                                                                          | 633 ms: 1.17x slower                                                                                                  |
| generators                 | 28.5 ms                                                                                                         | 33.4 ms: 1.17x slower                                                                                                 |
| nqueens                    | 74.6 ms                                                                                                         | 87.6 ms: 1.17x slower                                                                                                 |
| xml_etree_generate         | 86.0 ms                                                                                                         | 101 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.72 ms: 1.18x slower                                                                                                 |
| raytrace                   | 254 ms                                                                                                          | 304 ms: 1.20x slower                                                                                                  |
| deepcopy_memo              | 26.3 us                                                                                                         | 31.5 us: 1.20x slower                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 535 ms: 1.21x slower                                                                                                  |
| thrift                     | 778 us                                                                                                          | 940 us: 1.21x slower                                                                                                  |
| richards_super             | 48.8 ms                                                                                                         | 59.0 ms: 1.21x slower                                                                                                 |
| richards                   | 42.8 ms                                                                                                         | 52.0 ms: 1.22x slower                                                                                                 |
| connected_components       | 398 ms                                                                                                          | 487 ms: 1.22x slower                                                                                                  |
| fannkuch                   | 383 ms                                                                                                          | 470 ms: 1.23x slower                                                                                                  |
| sqlglot_v2_parse           | 1.14 ms                                                                                                         | 1.40 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.39 sec                                                                                                        | 2.94 sec: 1.23x slower                                                                                                |
| xml_etree_process          | 60.8 ms                                                                                                         | 75.0 ms: 1.23x slower                                                                                                 |
| typing_runtime_protocols   | 118 us                                                                                                          | 146 us: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 63.6 ms                                                                                                         | 79.0 ms: 1.24x slower                                                                                                 |
| python_startup             | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 99.7 ms                                                                                                         | 127 ms: 1.28x slower                                                                                                  |
| crypto_pyaes               | 69.6 ms                                                                                                         | 89.8 ms: 1.29x slower                                                                                                 |
| nbody                      | 94.3 ms                                                                                                         | 124 ms: 1.31x slower                                                                                                  |
| python_startup_no_site     | 6.94 ms                                                                                                         | 9.17 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 16.1 ms: 1.36x slower                                                                                                 |
| coverage                   | 82.7 ms                                                                                                         | 114 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.102x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x