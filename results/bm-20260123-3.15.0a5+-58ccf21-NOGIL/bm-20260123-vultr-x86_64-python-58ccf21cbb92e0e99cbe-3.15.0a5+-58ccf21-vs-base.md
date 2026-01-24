# Results vs. base

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: linux-x86_64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                            | 278 ms: 1.12x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 2.72 sec: 1.07x slower                                                                                                  |
| html5lib       | 59.0 ms                                                                                                           | 67.2 ms: 1.14x slower                                                                                                   |
| sphinx         | 957 ms                                                                                                            | 1.06 sec: 1.11x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                                                            | 512 ms: 1.06x faster                                                                                                    |
| coroutines                 | 24.2 ms                                                                                                           | 23.2 ms: 1.04x faster                                                                                                   |
| async_tree_none_tg         | 249 ms                                                                                                            | 261 ms: 1.05x slower                                                                                                    |
| async_tree_io_tg           | 559 ms                                                                                                            | 603 ms: 1.08x slower                                                                                                    |
| async_tree_memoization_tg  | 295 ms                                                                                                            | 324 ms: 1.10x slower                                                                                                    |
| async_generators           | 338 ms                                                                                                            | 375 ms: 1.11x slower                                                                                                    |
| async_tree_io              | 546 ms                                                                                                            | 621 ms: 1.14x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                                                            | 572 ms: 1.16x slower                                                                                                    |
| async_tree_memoization     | 304 ms                                                                                                            | 354 ms: 1.16x slower                                                                                                    |
| async_tree_none            | 242 ms                                                                                                            | 282 ms: 1.16x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                            | 597 ms: 1.22x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 70.6 ms                                                                                                           | 72.7 ms: 1.03x slower                                                                                                   |
| pidigits       | 193 ms                                                                                                            | 230 ms: 1.19x slower                                                                                                    |
| nbody          | 90.9 ms                                                                                                           | 122 ms: 1.35x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                                                                           | 21.2 ms: 1.05x faster                                                                                                   |
| regex_dna      | 173 ms                                                                                                            | 181 ms: 1.04x slower                                                                                                    |
| regex_compile  | 122 ms                                                                                                            | 140 ms: 1.15x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 85.1 ms                                                                                                           | 88.2 ms: 1.04x slower                                                                                                   |
| tomli_loads          | 1.83 sec                                                                                                          | 1.96 sec: 1.07x slower                                                                                                  |
| pickle_pure_python   | 304 us                                                                                                            | 333 us: 1.09x slower                                                                                                    |
| unpickle_pure_python | 212 us                                                                                                            | 234 us: 1.10x slower                                                                                                    |
| json_dumps           | 9.54 ms                                                                                                           | 11.0 ms: 1.15x slower                                                                                                   |
| json_loads           | 27.7 us                                                                                                           | 32.1 us: 1.16x slower                                                                                                   |
| xml_etree_generate   | 82.0 ms                                                                                                           | 95.6 ms: 1.17x slower                                                                                                   |
| xml_etree_process    | 57.5 ms                                                                                                           | 68.4 ms: 1.19x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.9 ms: 1.28x slower                                                                                                   |
| python_startup_no_site | 7.27 ms                                                                                                           | 9.69 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.31x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                                                           | 40.2 ms: 1.16x slower                                                                                                   |
| genshi_xml      | 48.8 ms                                                                                                           | 57.0 ms: 1.17x slower                                                                                                   |
| genshi_text     | 21.3 ms                                                                                                           | 26.9 ms: 1.26x slower                                                                                                   |
| mako            | 12.0 ms                                                                                                           | 15.6 ms: 1.30x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.22x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json | results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 255 ms                                                                                                            | 7.04 ms: 36.18x faster                                                                                                  |
| gc_traversal               | 4.29 ms                                                                                                           | 1.94 ms: 2.21x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.49 ms: 1.25x faster                                                                                                   |
| sqlite_synth               | 2.26 us                                                                                                           | 2.06 us: 1.10x faster                                                                                                   |
| asyncio_websockets         | 544 ms                                                                                                            | 512 ms: 1.06x faster                                                                                                    |
| regex_v8                   | 22.3 ms                                                                                                           | 21.2 ms: 1.05x faster                                                                                                   |
| coroutines                 | 24.2 ms                                                                                                           | 23.2 ms: 1.04x faster                                                                                                   |
| logging_silent             | 103 ns                                                                                                            | 104 ns: 1.01x slower                                                                                                    |
| float                      | 70.6 ms                                                                                                           | 72.7 ms: 1.03x slower                                                                                                   |
| xml_etree_iterparse        | 85.1 ms                                                                                                           | 88.2 ms: 1.04x slower                                                                                                   |
| pathlib                    | 17.3 ms                                                                                                           | 18.0 ms: 1.04x slower                                                                                                   |
| pycparser                  | 1.08 sec                                                                                                          | 1.12 sec: 1.04x slower                                                                                                  |
| regex_dna                  | 173 ms                                                                                                            | 181 ms: 1.04x slower                                                                                                    |
| bpe_tokeniser              | 4.20 sec                                                                                                          | 4.39 sec: 1.05x slower                                                                                                  |
| async_tree_none_tg         | 249 ms                                                                                                            | 261 ms: 1.05x slower                                                                                                    |
| sympy_expand               | 491 ms                                                                                                            | 516 ms: 1.05x slower                                                                                                    |
| dulwich_log                | 66.7 ms                                                                                                           | 70.8 ms: 1.06x slower                                                                                                   |
| pylint                     | 283 ms                                                                                                            | 302 ms: 1.07x slower                                                                                                    |
| docutils                   | 2.55 sec                                                                                                          | 2.72 sec: 1.07x slower                                                                                                  |
| tomli_loads                | 1.83 sec                                                                                                          | 1.96 sec: 1.07x slower                                                                                                  |
| async_tree_io_tg           | 559 ms                                                                                                            | 603 ms: 1.08x slower                                                                                                    |
| pprint_safe_repr           | 709 ms                                                                                                            | 767 ms: 1.08x slower                                                                                                    |
| subparsers                 | 9.28 ms                                                                                                           | 10.1 ms: 1.08x slower                                                                                                   |
| many_optionals             | 936 us                                                                                                            | 1.02 ms: 1.09x slower                                                                                                   |
| json                       | 4.98 ms                                                                                                           | 5.42 ms: 1.09x slower                                                                                                   |
| deltablue                  | 3.28 ms                                                                                                           | 3.58 ms: 1.09x slower                                                                                                   |
| pprint_pformat             | 1.45 sec                                                                                                          | 1.58 sec: 1.09x slower                                                                                                  |
| pickle_pure_python         | 304 us                                                                                                            | 333 us: 1.09x slower                                                                                                    |
| async_tree_memoization_tg  | 295 ms                                                                                                            | 324 ms: 1.10x slower                                                                                                    |
| unpickle_pure_python       | 212 us                                                                                                            | 234 us: 1.10x slower                                                                                                    |
| scimark_fft                | 308 ms                                                                                                            | 340 ms: 1.10x slower                                                                                                    |
| sphinx                     | 957 ms                                                                                                            | 1.06 sec: 1.11x slower                                                                                                  |
| async_generators           | 338 ms                                                                                                            | 375 ms: 1.11x slower                                                                                                    |
| nqueens                    | 79.7 ms                                                                                                           | 88.4 ms: 1.11x slower                                                                                                   |
| logging_simple             | 5.96 us                                                                                                           | 6.62 us: 1.11x slower                                                                                                   |
| logging_format             | 6.75 us                                                                                                           | 7.51 us: 1.11x slower                                                                                                   |
| chaos                      | 56.1 ms                                                                                                           | 62.5 ms: 1.11x slower                                                                                                   |
| 2to3                       | 249 ms                                                                                                            | 278 ms: 1.12x slower                                                                                                    |
| telco                      | 156 ms                                                                                                            | 175 ms: 1.12x slower                                                                                                    |
| sympy_str                  | 276 ms                                                                                                            | 310 ms: 1.12x slower                                                                                                    |
| deepcopy_reduce            | 2.54 us                                                                                                           | 2.85 us: 1.12x slower                                                                                                   |
| generators                 | 29.4 ms                                                                                                           | 33.1 ms: 1.13x slower                                                                                                   |
| pyflate                    | 411 ms                                                                                                            | 465 ms: 1.13x slower                                                                                                    |
| deepcopy                   | 230 us                                                                                                            | 260 us: 1.13x slower                                                                                                    |
| bench_thread_pool          | 1.30 ms                                                                                                           | 1.48 ms: 1.14x slower                                                                                                   |
| async_tree_io              | 546 ms                                                                                                            | 621 ms: 1.14x slower                                                                                                    |
| go                         | 105 ms                                                                                                            | 120 ms: 1.14x slower                                                                                                    |
| html5lib                   | 59.0 ms                                                                                                           | 67.2 ms: 1.14x slower                                                                                                   |
| deepcopy_memo              | 26.4 us                                                                                                           | 30.2 us: 1.14x slower                                                                                                   |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| regex_compile              | 122 ms                                                                                                            | 140 ms: 1.15x slower                                                                                                    |
| sympy_integrate            | 18.9 ms                                                                                                           | 21.7 ms: 1.15x slower                                                                                                   |
| comprehensions             | 16.0 us                                                                                                           | 18.4 us: 1.15x slower                                                                                                   |
| scimark_sor                | 104 ms                                                                                                            | 120 ms: 1.15x slower                                                                                                    |
| json_dumps                 | 9.54 ms                                                                                                           | 11.0 ms: 1.15x slower                                                                                                   |
| sympy_sum                  | 154 ms                                                                                                            | 177 ms: 1.15x slower                                                                                                    |
| thrift                     | 757 us                                                                                                            | 875 us: 1.16x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                                                            | 572 ms: 1.16x slower                                                                                                    |
| hexiom                     | 5.62 ms                                                                                                           | 6.50 ms: 1.16x slower                                                                                                   |
| django_template            | 34.7 ms                                                                                                           | 40.2 ms: 1.16x slower                                                                                                   |
| json_loads                 | 27.7 us                                                                                                           | 32.1 us: 1.16x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                           | 1.76 ms: 1.16x slower                                                                                                   |
| async_tree_memoization     | 304 ms                                                                                                            | 354 ms: 1.16x slower                                                                                                    |
| async_tree_none            | 242 ms                                                                                                            | 282 ms: 1.16x slower                                                                                                    |
| xml_etree_generate         | 82.0 ms                                                                                                           | 95.6 ms: 1.17x slower                                                                                                   |
| spectral_norm              | 92.8 ms                                                                                                           | 108 ms: 1.17x slower                                                                                                    |
| genshi_xml                 | 48.8 ms                                                                                                           | 57.0 ms: 1.17x slower                                                                                                   |
| raytrace                   | 252 ms                                                                                                            | 295 ms: 1.17x slower                                                                                                    |
| sqlglot_v2_optimize        | 50.7 ms                                                                                                           | 59.5 ms: 1.17x slower                                                                                                   |
| sqlglot_v2_parse           | 1.21 ms                                                                                                           | 1.43 ms: 1.18x slower                                                                                                   |
| typing_runtime_protocols   | 158 us                                                                                                            | 188 us: 1.19x slower                                                                                                    |
| xml_etree_process          | 57.5 ms                                                                                                           | 68.4 ms: 1.19x slower                                                                                                   |
| k_core                     | 1.85 sec                                                                                                          | 2.21 sec: 1.19x slower                                                                                                  |
| fannkuch                   | 381 ms                                                                                                            | 454 ms: 1.19x slower                                                                                                    |
| pidigits                   | 193 ms                                                                                                            | 230 ms: 1.19x slower                                                                                                    |
| sqlglot_v2_normalize       | 101 ms                                                                                                            | 121 ms: 1.20x slower                                                                                                    |
| scimark_lu                 | 107 ms                                                                                                            | 129 ms: 1.21x slower                                                                                                    |
| meteor_contest             | 102 ms                                                                                                            | 124 ms: 1.21x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                            | 597 ms: 1.22x slower                                                                                                    |
| richards_super             | 48.4 ms                                                                                                           | 58.9 ms: 1.22x slower                                                                                                   |
| richards                   | 42.1 ms                                                                                                           | 51.6 ms: 1.22x slower                                                                                                   |
| scimark_monte_carlo        | 63.1 ms                                                                                                           | 77.7 ms: 1.23x slower                                                                                                   |
| shortest_path              | 427 ms                                                                                                            | 530 ms: 1.24x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.33 ms                                                                                                           | 5.41 ms: 1.25x slower                                                                                                   |
| connected_components       | 386 ms                                                                                                            | 483 ms: 1.25x slower                                                                                                    |
| genshi_text                | 21.3 ms                                                                                                           | 26.9 ms: 1.26x slower                                                                                                   |
| crypto_pyaes               | 67.9 ms                                                                                                           | 86.3 ms: 1.27x slower                                                                                                   |
| python_startup             | 12.4 ms                                                                                                           | 15.9 ms: 1.28x slower                                                                                                   |
| mako                       | 12.0 ms                                                                                                           | 15.6 ms: 1.30x slower                                                                                                   |
| python_startup_no_site     | 7.27 ms                                                                                                           | 9.69 ms: 1.33x slower                                                                                                   |
| nbody                      | 90.9 ms                                                                                                           | 122 ms: 1.35x slower                                                                                                    |
| coverage                   | 81.0 ms                                                                                                           | 111 ms: 1.37x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, xml_etree_parse

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x