# Results vs. base

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: linux-x86_64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.095x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| docutils       | 2.56 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| html5lib       | 61.2 ms                                                                                                         | 66.8 ms: 1.09x slower                                                                                                 |
| sphinx         | 971 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 612 ms                                                                                                          | 510 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 258 ms                                                                                                          | 223 ms: 1.16x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 281 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 585 ms                                                                                                          | 536 ms: 1.09x faster                                                                                                  |
| async_tree_none            | 264 ms                                                                                                          | 253 ms: 1.04x faster                                                                                                  |
| async_tree_memoization     | 312 ms                                                                                                          | 308 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                                                          | 485 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                          | 509 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.5 ms                                                                                                         | 24.7 ms: 1.05x slower                                                                                                 |
| async_generators           | 338 ms                                                                                                          | 375 ms: 1.11x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                                                          | 192 ms: 1.13x faster                                                                                                  |
| float          | 71.8 ms                                                                                                         | 69.1 ms: 1.04x faster                                                                                                 |
| nbody          | 89.3 ms                                                                                                         | 126 ms: 1.41x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 20.8 ms                                                                                                         | 20.7 ms: 1.00x faster                                                                                                 |
| regex_effbot   | 2.60 ms                                                                                                         | 2.71 ms: 1.04x slower                                                                                                 |
| regex_dna      | 164 ms                                                                                                          | 175 ms: 1.07x slower                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.6 ms                                                                                                         | 87.1 ms: 1.06x faster                                                                                                 |
| xml_etree_parse      | 133 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| pickle_pure_python   | 306 us                                                                                                          | 341 us: 1.11x slower                                                                                                  |
| tomli_loads          | 1.93 sec                                                                                                        | 2.16 sec: 1.12x slower                                                                                                |
| unpickle_pure_python | 207 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| json_dumps           | 10.7 ms                                                                                                         | 12.1 ms: 1.13x slower                                                                                                 |
| json_loads           | 27.9 us                                                                                                         | 31.5 us: 1.13x slower                                                                                                 |
| xml_etree_generate   | 83.0 ms                                                                                                         | 96.5 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 57.4 ms                                                                                                         | 70.1 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 9.55 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.0 ms                                                                                                         | 40.2 ms: 1.15x slower                                                                                                 |
| genshi_xml      | 47.9 ms                                                                                                         | 57.4 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.8 ms                                                                                                         | 26.7 ms: 1.28x slower                                                                                                 |
| mako            | 11.6 ms                                                                                                         | 15.7 ms: 1.35x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json | results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.78 ms                                                                                                         | 1.95 ms: 2.45x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.53 ms: 1.27x faster                                                                                                 |
| async_tree_io_tg           | 612 ms                                                                                                          | 510 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 258 ms                                                                                                          | 223 ms: 1.16x faster                                                                                                  |
| pidigits                   | 217 ms                                                                                                          | 192 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 281 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.27 us                                                                                                         | 2.06 us: 1.10x faster                                                                                                 |
| async_tree_io              | 585 ms                                                                                                          | 536 ms: 1.09x faster                                                                                                  |
| xml_etree_iterparse        | 92.6 ms                                                                                                         | 87.1 ms: 1.06x faster                                                                                                 |
| async_tree_none            | 264 ms                                                                                                          | 253 ms: 1.04x faster                                                                                                  |
| float                      | 71.8 ms                                                                                                         | 69.1 ms: 1.04x faster                                                                                                 |
| xml_etree_parse            | 133 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| async_tree_memoization     | 312 ms                                                                                                          | 308 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                                                          | 485 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| regex_v8                   | 20.8 ms                                                                                                         | 20.7 ms: 1.00x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                          | 509 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| regex_effbot               | 2.60 ms                                                                                                         | 2.71 ms: 1.04x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.04x slower                                                                                                |
| json                       | 5.14 ms                                                                                                         | 5.37 ms: 1.04x slower                                                                                                 |
| coroutines                 | 23.5 ms                                                                                                         | 24.7 ms: 1.05x slower                                                                                                 |
| bench_mp_pool              | 102 ms                                                                                                          | 108 ms: 1.05x slower                                                                                                  |
| docutils                   | 2.56 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| regex_dna                  | 164 ms                                                                                                          | 175 ms: 1.07x slower                                                                                                  |
| sphinx                     | 971 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| dulwich_log                | 66.3 ms                                                                                                         | 71.5 ms: 1.08x slower                                                                                                 |
| logging_silent             | 96.2 ns                                                                                                         | 104 ns: 1.08x slower                                                                                                  |
| generators                 | 28.1 ms                                                                                                         | 30.5 ms: 1.08x slower                                                                                                 |
| html5lib                   | 61.2 ms                                                                                                         | 66.8 ms: 1.09x slower                                                                                                 |
| pylint                     | 281 ms                                                                                                          | 308 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| many_optionals             | 1.21 ms                                                                                                         | 1.34 ms: 1.11x slower                                                                                                 |
| async_generators           | 338 ms                                                                                                          | 375 ms: 1.11x slower                                                                                                  |
| pickle_pure_python         | 306 us                                                                                                          | 341 us: 1.11x slower                                                                                                  |
| telco                      | 157 ms                                                                                                          | 176 ms: 1.12x slower                                                                                                  |
| tomli_loads                | 1.93 sec                                                                                                        | 2.16 sec: 1.12x slower                                                                                                |
| unpickle_pure_python       | 207 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| sympy_expand               | 464 ms                                                                                                          | 522 ms: 1.13x slower                                                                                                  |
| json_dumps                 | 10.7 ms                                                                                                         | 12.1 ms: 1.13x slower                                                                                                 |
| scimark_fft                | 326 ms                                                                                                          | 368 ms: 1.13x slower                                                                                                  |
| hexiom                     | 5.66 ms                                                                                                         | 6.38 ms: 1.13x slower                                                                                                 |
| json_loads                 | 27.9 us                                                                                                         | 31.5 us: 1.13x slower                                                                                                 |
| chaos                      | 55.8 ms                                                                                                         | 63.5 ms: 1.14x slower                                                                                                 |
| pprint_safe_repr           | 686 ms                                                                                                          | 781 ms: 1.14x slower                                                                                                  |
| 2to3                       | 249 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| comprehensions             | 15.4 us                                                                                                         | 17.6 us: 1.14x slower                                                                                                 |
| subparsers                 | 42.8 ms                                                                                                         | 48.8 ms: 1.14x slower                                                                                                 |
| nqueens                    | 76.5 ms                                                                                                         | 87.6 ms: 1.15x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| django_template            | 35.0 ms                                                                                                         | 40.2 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 50.1 ms                                                                                                         | 57.7 ms: 1.15x slower                                                                                                 |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.62 sec: 1.15x slower                                                                                                |
| scimark_sor                | 107 ms                                                                                                          | 124 ms: 1.15x slower                                                                                                  |
| deepcopy_reduce            | 2.64 us                                                                                                         | 3.05 us: 1.16x slower                                                                                                 |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.9 ms                                                                                                         | 115 ms: 1.16x slower                                                                                                  |
| go                         | 104 ms                                                                                                          | 121 ms: 1.16x slower                                                                                                  |
| sympy_str                  | 269 ms                                                                                                          | 312 ms: 1.16x slower                                                                                                  |
| xml_etree_generate         | 83.0 ms                                                                                                         | 96.5 ms: 1.16x slower                                                                                                 |
| pyflate                    | 398 ms                                                                                                          | 464 ms: 1.17x slower                                                                                                  |
| sympy_sum                  | 154 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.9 ms                                                                                                         | 22.1 ms: 1.17x slower                                                                                                 |
| spectral_norm              | 96.6 ms                                                                                                         | 113 ms: 1.17x slower                                                                                                  |
| thrift                     | 747 us                                                                                                          | 881 us: 1.18x slower                                                                                                  |
| logging_simple             | 5.84 us                                                                                                         | 6.94 us: 1.19x slower                                                                                                 |
| deepcopy                   | 250 us                                                                                                          | 298 us: 1.19x slower                                                                                                  |
| scimark_lu                 | 109 ms                                                                                                          | 130 ms: 1.19x slower                                                                                                  |
| deltablue                  | 3.07 ms                                                                                                         | 3.67 ms: 1.20x slower                                                                                                 |
| genshi_xml                 | 47.9 ms                                                                                                         | 57.4 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 379 ms                                                                                                          | 455 ms: 1.20x slower                                                                                                  |
| meteor_contest             | 99.1 ms                                                                                                         | 119 ms: 1.20x slower                                                                                                  |
| raytrace                   | 249 ms                                                                                                          | 299 ms: 1.20x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.82 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.47 ms: 1.22x slower                                                                                                 |
| shortest_path              | 442 ms                                                                                                          | 540 ms: 1.22x slower                                                                                                  |
| xml_etree_process          | 57.4 ms                                                                                                         | 70.1 ms: 1.22x slower                                                                                                 |
| logging_format             | 6.60 us                                                                                                         | 8.10 us: 1.23x slower                                                                                                 |
| deepcopy_memo              | 28.3 us                                                                                                         | 34.9 us: 1.23x slower                                                                                                 |
| connected_components       | 398 ms                                                                                                          | 493 ms: 1.24x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.53 ms                                                                                                         | 5.62 ms: 1.24x slower                                                                                                 |
| typing_runtime_protocols   | 154 us                                                                                                          | 192 us: 1.24x slower                                                                                                  |
| richards                   | 41.0 ms                                                                                                         | 51.1 ms: 1.25x slower                                                                                                 |
| richards_super             | 47.2 ms                                                                                                         | 58.9 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 68.0 ms                                                                                                         | 86.4 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.8 ms                                                                                                         | 26.7 ms: 1.28x slower                                                                                                 |
| scimark_monte_carlo        | 61.1 ms                                                                                                         | 78.8 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                         | 9.55 ms: 1.32x slower                                                                                                 |
| mako                       | 11.6 ms                                                                                                         | 15.7 ms: 1.35x slower                                                                                                 |
| coverage                   | 81.5 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| nbody                      | 89.3 ms                                                                                                         | 126 ms: 1.41x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.16 ms: 3.01x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.095x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.19x