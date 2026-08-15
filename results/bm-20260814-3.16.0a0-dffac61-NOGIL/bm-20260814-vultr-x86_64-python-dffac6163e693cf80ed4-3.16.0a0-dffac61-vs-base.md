# Results vs. base

- fork: python
- ref: dffac6163e693cf80ed4
- machine: linux-x86_64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 263 ms                                                                                                          | 297 ms: 1.13x slower                                                                                                  |
| docutils       | 2.40 sec                                                                                                        | 2.91 sec: 1.21x slower                                                                                                |
| html5lib       | 60.0 ms                                                                                                         | 65.7 ms: 1.09x slower                                                                                                 |
| sphinx         | 1.00 sec                                                                                                        | 1.09 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 761 ms                                                                                                          | 693 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 511 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 728 ms                                                                                                          | 704 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 23.9 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                                                          | 583 ms: 1.03x slower                                                                                                  |
| async_tree_memoization_tg  | 368 ms                                                                                                          | 401 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 304 ms                                                                                                          | 334 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 602 ms: 1.11x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 425 ms: 1.12x slower                                                                                                  |
| async_generators           | 349 ms                                                                                                          | 394 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 298 ms                                                                                                          | 345 ms: 1.16x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| float          | 72.8 ms                                                                                                         | 83.4 ms: 1.15x slower                                                                                                 |
| nbody          | 88.1 ms                                                                                                         | 120 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.14x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 192 ms                                                                                                          | 175 ms: 1.10x faster                                                                                                  |
| regex_v8       | 21.9 ms                                                                                                         | 20.1 ms: 1.09x faster                                                                                                 |
| regex_effbot   | 2.88 ms                                                                                                         | 2.88 ms: 1.00x faster                                                                                                 |
| regex_compile  | 149 ms                                                                                                          | 169 ms: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 91.5 ms                                                                                                         | 94.9 ms: 1.04x slower                                                                                                 |
| tomli_loads          | 1.81 sec                                                                                                        | 1.91 sec: 1.06x slower                                                                                                |
| pickle_pure_python   | 312 us                                                                                                          | 333 us: 1.07x slower                                                                                                  |
| json_dumps           | 9.29 ms                                                                                                         | 10.2 ms: 1.09x slower                                                                                                 |
| unpickle_pure_python | 213 us                                                                                                          | 239 us: 1.12x slower                                                                                                  |
| xml_etree_generate   | 88.5 ms                                                                                                         | 99.4 ms: 1.12x slower                                                                                                 |
| json_loads           | 27.3 us                                                                                                         | 30.7 us: 1.13x slower                                                                                                 |
| xml_etree_process    | 62.5 ms                                                                                                         | 75.1 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.24x slower                                                                                                 |
| python_startup_no_site | 7.06 ms                                                                                                         | 9.23 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.27x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                         | 40.5 ms: 1.11x slower                                                                                                 |
| mako            | 12.3 ms                                                                                                         | 16.1 ms: 1.31x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.20x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json | results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 249 ms                                                                                                          | 6.66 ms: 37.45x faster                                                                                                |
| gc_traversal               | 4.03 ms                                                                                                         | 1.78 ms: 2.26x faster                                                                                                 |
| create_gc_cycles           | 1.65 ms                                                                                                         | 1.35 ms: 1.23x faster                                                                                                 |
| sqlite_synth               | 2.19 us                                                                                                         | 1.92 us: 1.14x faster                                                                                                 |
| regex_dna                  | 192 ms                                                                                                          | 175 ms: 1.10x faster                                                                                                  |
| async_tree_io_tg           | 761 ms                                                                                                          | 693 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 21.9 ms                                                                                                         | 20.1 ms: 1.09x faster                                                                                                 |
| asyncio_websockets         | 544 ms                                                                                                          | 511 ms: 1.06x faster                                                                                                  |
| pidigits                   | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| async_tree_io              | 728 ms                                                                                                          | 704 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| pathlib                    | 17.9 ms                                                                                                         | 17.7 ms: 1.01x faster                                                                                                 |
| regex_effbot               | 2.88 ms                                                                                                         | 2.88 ms: 1.00x faster                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                        | 1.14 sec: 1.01x slower                                                                                                |
| coroutines                 | 23.4 ms                                                                                                         | 23.9 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                                                          | 583 ms: 1.03x slower                                                                                                  |
| xml_etree_iterparse        | 91.5 ms                                                                                                         | 94.9 ms: 1.04x slower                                                                                                 |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| logging_silent             | 98.7 ns                                                                                                         | 103 ns: 1.04x slower                                                                                                  |
| dulwich_log                | 67.8 ms                                                                                                         | 71.6 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.81 sec                                                                                                        | 1.91 sec: 1.06x slower                                                                                                |
| pickle_pure_python         | 312 us                                                                                                          | 333 us: 1.07x slower                                                                                                  |
| generators                 | 29.9 ms                                                                                                         | 32.0 ms: 1.07x slower                                                                                                 |
| deltablue                  | 3.41 ms                                                                                                         | 3.67 ms: 1.08x slower                                                                                                 |
| many_optionals             | 925 us                                                                                                          | 998 us: 1.08x slower                                                                                                  |
| telco                      | 164 ms                                                                                                          | 177 ms: 1.08x slower                                                                                                  |
| scimark_lu                 | 119 ms                                                                                                          | 129 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 368 ms                                                                                                          | 401 ms: 1.09x slower                                                                                                  |
| sphinx                     | 1.00 sec                                                                                                        | 1.09 sec: 1.09x slower                                                                                                |
| json_dumps                 | 9.29 ms                                                                                                         | 10.2 ms: 1.09x slower                                                                                                 |
| html5lib                   | 60.0 ms                                                                                                         | 65.7 ms: 1.09x slower                                                                                                 |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.48 ms: 1.10x slower                                                                                                 |
| k_core                     | 2.06 sec                                                                                                        | 2.27 sec: 1.10x slower                                                                                                |
| scimark_sor                | 109 ms                                                                                                          | 120 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 304 ms                                                                                                          | 334 ms: 1.10x slower                                                                                                  |
| scimark_fft                | 314 ms                                                                                                          | 346 ms: 1.10x slower                                                                                                  |
| pprint_safe_repr           | 732 ms                                                                                                          | 808 ms: 1.10x slower                                                                                                  |
| sqlglot_v2_optimize        | 52.1 ms                                                                                                         | 57.5 ms: 1.10x slower                                                                                                 |
| django_template            | 36.6 ms                                                                                                         | 40.5 ms: 1.11x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 602 ms: 1.11x slower                                                                                                  |
| json                       | 4.86 ms                                                                                                         | 5.40 ms: 1.11x slower                                                                                                 |
| chaos                      | 54.2 ms                                                                                                         | 60.1 ms: 1.11x slower                                                                                                 |
| sympy_expand               | 477 ms                                                                                                          | 531 ms: 1.11x slower                                                                                                  |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 114 ms: 1.11x slower                                                                                                  |
| subparsers                 | 9.19 ms                                                                                                         | 10.2 ms: 1.11x slower                                                                                                 |
| go                         | 106 ms                                                                                                          | 119 ms: 1.12x slower                                                                                                  |
| deepcopy_reduce            | 2.61 us                                                                                                         | 2.93 us: 1.12x slower                                                                                                 |
| pprint_pformat             | 1.49 sec                                                                                                        | 1.68 sec: 1.12x slower                                                                                                |
| unpickle_pure_python       | 213 us                                                                                                          | 239 us: 1.12x slower                                                                                                  |
| xml_etree_generate         | 88.5 ms                                                                                                         | 99.4 ms: 1.12x slower                                                                                                 |
| deepcopy                   | 237 us                                                                                                          | 266 us: 1.12x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 425 ms: 1.12x slower                                                                                                  |
| logging_simple             | 6.23 us                                                                                                         | 7.00 us: 1.12x slower                                                                                                 |
| logging_format             | 7.12 us                                                                                                         | 8.01 us: 1.12x slower                                                                                                 |
| sympy_str                  | 280 ms                                                                                                          | 315 ms: 1.13x slower                                                                                                  |
| json_loads                 | 27.3 us                                                                                                         | 30.7 us: 1.13x slower                                                                                                 |
| async_generators           | 349 ms                                                                                                          | 394 ms: 1.13x slower                                                                                                  |
| comprehensions             | 15.7 us                                                                                                         | 17.8 us: 1.13x slower                                                                                                 |
| sympy_integrate            | 19.2 ms                                                                                                         | 21.7 ms: 1.13x slower                                                                                                 |
| regex_compile              | 149 ms                                                                                                          | 169 ms: 1.13x slower                                                                                                  |
| 2to3                       | 263 ms                                                                                                          | 297 ms: 1.13x slower                                                                                                  |
| sympy_sum                  | 159 ms                                                                                                          | 180 ms: 1.13x slower                                                                                                  |
| pylint                     | 115 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| richards                   | 45.2 ms                                                                                                         | 51.5 ms: 1.14x slower                                                                                                 |
| mdp                        | 1.13 sec                                                                                                        | 1.29 sec: 1.14x slower                                                                                                |
| hexiom                     | 5.69 ms                                                                                                         | 6.51 ms: 1.14x slower                                                                                                 |
| float                      | 72.8 ms                                                                                                         | 83.4 ms: 1.15x slower                                                                                                 |
| raytrace                   | 254 ms                                                                                                          | 291 ms: 1.15x slower                                                                                                  |
| richards_super             | 51.5 ms                                                                                                         | 59.2 ms: 1.15x slower                                                                                                 |
| async_tree_none            | 298 ms                                                                                                          | 345 ms: 1.16x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.52 ms                                                                                                         | 5.25 ms: 1.16x slower                                                                                                 |
| deepcopy_memo              | 26.7 us                                                                                                         | 31.0 us: 1.16x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.72 ms: 1.17x slower                                                                                                 |
| pyflate                    | 387 ms                                                                                                          | 455 ms: 1.18x slower                                                                                                  |
| nqueens                    | 73.4 ms                                                                                                         | 86.8 ms: 1.18x slower                                                                                                 |
| thrift                     | 783 us                                                                                                          | 929 us: 1.19x slower                                                                                                  |
| typing_runtime_protocols   | 122 us                                                                                                          | 145 us: 1.19x slower                                                                                                  |
| spectral_norm              | 91.1 ms                                                                                                         | 109 ms: 1.20x slower                                                                                                  |
| xml_etree_process          | 62.5 ms                                                                                                         | 75.1 ms: 1.20x slower                                                                                                 |
| meteor_contest             | 103 ms                                                                                                          | 124 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.40 ms: 1.21x slower                                                                                                 |
| docutils                   | 2.40 sec                                                                                                        | 2.91 sec: 1.21x slower                                                                                                |
| scimark_monte_carlo        | 63.5 ms                                                                                                         | 77.3 ms: 1.22x slower                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 541 ms: 1.22x slower                                                                                                  |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.24x slower                                                                                                 |
| connected_components       | 395 ms                                                                                                          | 496 ms: 1.26x slower                                                                                                  |
| fannkuch                   | 369 ms                                                                                                          | 465 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 68.3 ms                                                                                                         | 88.7 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.06 ms                                                                                                         | 9.23 ms: 1.31x slower                                                                                                 |
| mako                       | 12.3 ms                                                                                                         | 16.1 ms: 1.31x slower                                                                                                 |
| nbody                      | 88.1 ms                                                                                                         | 120 ms: 1.37x slower                                                                                                  |
| coverage                   | 83.4 ms                                                                                                         | 115 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.18x