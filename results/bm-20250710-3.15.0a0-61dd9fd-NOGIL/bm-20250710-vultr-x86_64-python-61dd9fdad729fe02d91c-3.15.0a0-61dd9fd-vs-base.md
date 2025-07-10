# Results vs. base

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: linux-x86_64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| docutils       | 2.55 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| html5lib       | 61.2 ms                                                                                                         | 66.0 ms: 1.08x slower                                                                                                 |
| sphinx         | 971 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 613 ms                                                                                                          | 523 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 228 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 598 ms                                                                                                          | 549 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 286 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                                                          | 490 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                          | 517 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.0 ms                                                                                                         | 24.9 ms: 1.08x slower                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 372 ms: 1.10x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 70.8 ms                                                                                                         | 70.4 ms: 1.01x faster                                                                                                 |
| pidigits       | 195 ms                                                                                                          | 204 ms: 1.05x slower                                                                                                  |
| nbody          | 93.6 ms                                                                                                         | 125 ms: 1.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                                                                         | 21.5 ms: 1.07x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 181 ms: 1.03x slower                                                                                                  |
| regex_effbot   | 2.72 ms                                                                                                         | 2.85 ms: 1.05x slower                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.9 ms                                                                                                         | 87.1 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| json_loads           | 28.7 us                                                                                                         | 31.2 us: 1.09x slower                                                                                                 |
| unpickle_pure_python | 211 us                                                                                                          | 231 us: 1.09x slower                                                                                                  |
| pickle_pure_python   | 309 us                                                                                                          | 339 us: 1.10x slower                                                                                                  |
| json_dumps           | 10.9 ms                                                                                                         | 12.2 ms: 1.12x slower                                                                                                 |
| tomli_loads          | 1.93 sec                                                                                                        | 2.18 sec: 1.13x slower                                                                                                |
| xml_etree_generate   | 82.7 ms                                                                                                         | 96.2 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 57.7 ms                                                                                                         | 69.1 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.35 ms                                                                                                         | 9.58 ms: 1.30x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                                                                         | 39.5 ms: 1.16x slower                                                                                                 |
| genshi_xml      | 48.4 ms                                                                                                         | 57.5 ms: 1.19x slower                                                                                                 |
| genshi_text     | 20.6 ms                                                                                                         | 26.9 ms: 1.31x slower                                                                                                 |
| mako            | 11.5 ms                                                                                                         | 15.8 ms: 1.37x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json | results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                                                         | 1.90 ms: 2.31x faster                                                                                                 |
| create_gc_cycles           | 1.97 ms                                                                                                         | 1.48 ms: 1.34x faster                                                                                                 |
| async_tree_io_tg           | 613 ms                                                                                                          | 523 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 228 ms: 1.12x faster                                                                                                  |
| sqlite_synth               | 2.24 us                                                                                                         | 2.05 us: 1.09x faster                                                                                                 |
| async_tree_io              | 598 ms                                                                                                          | 549 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 286 ms: 1.08x faster                                                                                                  |
| regex_v8                   | 23.1 ms                                                                                                         | 21.5 ms: 1.07x faster                                                                                                 |
| xml_etree_iterparse        | 92.9 ms                                                                                                         | 87.1 ms: 1.07x faster                                                                                                 |
| xml_etree_parse            | 132 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                                                          | 490 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| float                      | 70.8 ms                                                                                                         | 70.4 ms: 1.01x faster                                                                                                 |
| regex_dna                  | 176 ms                                                                                                          | 181 ms: 1.03x slower                                                                                                  |
| logging_silent             | 99.3 ns                                                                                                         | 103 ns: 1.03x slower                                                                                                  |
| json                       | 5.15 ms                                                                                                         | 5.33 ms: 1.03x slower                                                                                                 |
| pidigits                   | 195 ms                                                                                                          | 204 ms: 1.05x slower                                                                                                  |
| regex_effbot               | 2.72 ms                                                                                                         | 2.85 ms: 1.05x slower                                                                                                 |
| pycparser                  | 1.10 sec                                                                                                        | 1.15 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 108 ms: 1.05x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                          | 517 ms: 1.05x slower                                                                                                  |
| docutils                   | 2.55 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| bpe_tokeniser              | 4.17 sec                                                                                                        | 4.44 sec: 1.06x slower                                                                                                |
| html5lib                   | 61.2 ms                                                                                                         | 66.0 ms: 1.08x slower                                                                                                 |
| sphinx                     | 971 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| coroutines                 | 23.0 ms                                                                                                         | 24.9 ms: 1.08x slower                                                                                                 |
| json_loads                 | 28.7 us                                                                                                         | 31.2 us: 1.09x slower                                                                                                 |
| many_optionals             | 1.04 ms                                                                                                         | 1.13 ms: 1.09x slower                                                                                                 |
| unpickle_pure_python       | 211 us                                                                                                          | 231 us: 1.09x slower                                                                                                  |
| k_core                     | 2.04 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| dulwich_log                | 65.8 ms                                                                                                         | 72.4 ms: 1.10x slower                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 372 ms: 1.10x slower                                                                                                  |
| pickle_pure_python         | 309 us                                                                                                          | 339 us: 1.10x slower                                                                                                  |
| spectral_norm              | 98.8 ms                                                                                                         | 109 ms: 1.10x slower                                                                                                  |
| scimark_fft                | 338 ms                                                                                                          | 374 ms: 1.11x slower                                                                                                  |
| sympy_expand               | 471 ms                                                                                                          | 522 ms: 1.11x slower                                                                                                  |
| pylint                     | 279 ms                                                                                                          | 310 ms: 1.11x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 178 ms: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 695 ms                                                                                                          | 777 ms: 1.12x slower                                                                                                  |
| json_dumps                 | 10.9 ms                                                                                                         | 12.2 ms: 1.12x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.93 ms                                                                                                         | 5.54 ms: 1.12x slower                                                                                                 |
| scimark_sor                | 111 ms                                                                                                          | 125 ms: 1.13x slower                                                                                                  |
| hexiom                     | 5.63 ms                                                                                                         | 6.34 ms: 1.13x slower                                                                                                 |
| nqueens                    | 78.1 ms                                                                                                         | 88.0 ms: 1.13x slower                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 17.6 us: 1.13x slower                                                                                                 |
| subparsers                 | 25.1 ms                                                                                                         | 28.4 ms: 1.13x slower                                                                                                 |
| 2to3                       | 251 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| tomli_loads                | 1.93 sec                                                                                                        | 2.18 sec: 1.13x slower                                                                                                |
| generators                 | 27.7 ms                                                                                                         | 31.5 ms: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.42 sec                                                                                                        | 1.61 sec: 1.14x slower                                                                                                |
| chaos                      | 55.7 ms                                                                                                         | 63.7 ms: 1.14x slower                                                                                                 |
| scimark_lu                 | 113 ms                                                                                                          | 129 ms: 1.14x slower                                                                                                  |
| deltablue                  | 3.10 ms                                                                                                         | 3.56 ms: 1.15x slower                                                                                                 |
| thrift                     | 763 us                                                                                                          | 878 us: 1.15x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.15 sec                                                                                                        | 1.33 sec: 1.15x slower                                                                                                |
| django_template            | 34.1 ms                                                                                                         | 39.5 ms: 1.16x slower                                                                                                 |
| xml_etree_generate         | 82.7 ms                                                                                                         | 96.2 ms: 1.16x slower                                                                                                 |
| go                         | 104 ms                                                                                                          | 121 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 58.2 ms: 1.17x slower                                                                                                 |
| sympy_str                  | 269 ms                                                                                                          | 314 ms: 1.17x slower                                                                                                  |
| deepcopy                   | 251 us                                                                                                          | 294 us: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.1 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 180 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.4 ms                                                                                                         | 116 ms: 1.18x slower                                                                                                  |
| pyflate                    | 396 ms                                                                                                          | 467 ms: 1.18x slower                                                                                                  |
| deepcopy_memo              | 29.2 us                                                                                                         | 34.7 us: 1.19x slower                                                                                                 |
| logging_simple             | 5.88 us                                                                                                         | 6.98 us: 1.19x slower                                                                                                 |
| genshi_xml                 | 48.4 ms                                                                                                         | 57.5 ms: 1.19x slower                                                                                                 |
| meteor_contest             | 98.7 ms                                                                                                         | 118 ms: 1.19x slower                                                                                                  |
| logging_format             | 6.61 us                                                                                                         | 7.88 us: 1.19x slower                                                                                                 |
| deepcopy_reduce            | 2.62 us                                                                                                         | 3.12 us: 1.19x slower                                                                                                 |
| xml_etree_process          | 57.7 ms                                                                                                         | 69.1 ms: 1.20x slower                                                                                                 |
| raytrace                   | 254 ms                                                                                                          | 307 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.83 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.47 ms: 1.21x slower                                                                                                 |
| shortest_path              | 441 ms                                                                                                          | 535 ms: 1.21x slower                                                                                                  |
| fannkuch                   | 380 ms                                                                                                          | 463 ms: 1.22x slower                                                                                                  |
| connected_components       | 399 ms                                                                                                          | 489 ms: 1.22x slower                                                                                                  |
| typing_runtime_protocols   | 152 us                                                                                                          | 188 us: 1.24x slower                                                                                                  |
| richards                   | 40.9 ms                                                                                                         | 51.3 ms: 1.25x slower                                                                                                 |
| crypto_pyaes               | 68.2 ms                                                                                                         | 85.7 ms: 1.26x slower                                                                                                 |
| scimark_monte_carlo        | 62.3 ms                                                                                                         | 78.5 ms: 1.26x slower                                                                                                 |
| richards_super             | 46.6 ms                                                                                                         | 58.8 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.7 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site     | 7.35 ms                                                                                                         | 9.58 ms: 1.30x slower                                                                                                 |
| genshi_text                | 20.6 ms                                                                                                         | 26.9 ms: 1.31x slower                                                                                                 |
| nbody                      | 93.6 ms                                                                                                         | 125 ms: 1.33x slower                                                                                                  |
| coverage                   | 81.9 ms                                                                                                         | 112 ms: 1.37x slower                                                                                                  |
| mako                       | 11.5 ms                                                                                                         | 15.8 ms: 1.37x slower                                                                                                 |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.15 ms: 3.01x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (3): pathlib, async_tree_memoization, async_tree_none

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x