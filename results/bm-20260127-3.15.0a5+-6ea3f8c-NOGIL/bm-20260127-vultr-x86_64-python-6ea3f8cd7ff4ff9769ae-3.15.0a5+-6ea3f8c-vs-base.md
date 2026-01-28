# Results vs. base

- fork: python
- ref: 6ea3f8cd7ff4ff9769ae
- machine: linux-x86_64
- commit hash: 6ea3f8c
- commit date: 2026-01-27
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                                                            | 280 ms: 1.13x slower                                                                                                    |
| docutils       | 2.56 sec                                                                                                          | 2.75 sec: 1.07x slower                                                                                                  |
| html5lib       | 59.7 ms                                                                                                           | 66.3 ms: 1.11x slower                                                                                                   |
| sphinx         | 963 ms                                                                                                            | 1.05 sec: 1.09x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                                                            | 511 ms: 1.07x faster                                                                                                    |
| async_tree_io_tg           | 564 ms                                                                                                            | 603 ms: 1.07x slower                                                                                                    |
| async_tree_none_tg         | 246 ms                                                                                                            | 267 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                                                            | 537 ms: 1.09x slower                                                                                                    |
| async_generators           | 341 ms                                                                                                            | 373 ms: 1.09x slower                                                                                                    |
| async_tree_memoization_tg  | 293 ms                                                                                                            | 331 ms: 1.13x slower                                                                                                    |
| async_tree_io              | 552 ms                                                                                                            | 627 ms: 1.14x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                            | 561 ms: 1.14x slower                                                                                                    |
| async_tree_none            | 244 ms                                                                                                            | 287 ms: 1.17x slower                                                                                                    |
| async_tree_memoization     | 302 ms                                                                                                            | 359 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 202 ms                                                                                                            | 202 ms: 1.00x slower                                                                                                    |
| float          | 70.9 ms                                                                                                           | 73.5 ms: 1.04x slower                                                                                                   |
| nbody          | 90.8 ms                                                                                                           | 127 ms: 1.40x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.4 ms                                                                                                           | 21.2 ms: 1.06x faster                                                                                                   |
| regex_dna      | 173 ms                                                                                                            | 175 ms: 1.01x slower                                                                                                    |
| regex_effbot   | 2.75 ms                                                                                                           | 2.80 ms: 1.02x slower                                                                                                   |
| regex_compile  | 123 ms                                                                                                            | 140 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 131 ms                                                                                                            | 131 ms: 1.00x slower                                                                                                    |
| xml_etree_iterparse  | 84.4 ms                                                                                                           | 87.9 ms: 1.04x slower                                                                                                   |
| pickle_pure_python   | 309 us                                                                                                            | 334 us: 1.08x slower                                                                                                    |
| tomli_loads          | 1.82 sec                                                                                                          | 1.98 sec: 1.09x slower                                                                                                  |
| unpickle_pure_python | 213 us                                                                                                            | 236 us: 1.11x slower                                                                                                    |
| json_dumps           | 9.73 ms                                                                                                           | 11.1 ms: 1.14x slower                                                                                                   |
| json_loads           | 28.1 us                                                                                                           | 32.4 us: 1.15x slower                                                                                                   |
| xml_etree_generate   | 82.1 ms                                                                                                           | 96.2 ms: 1.17x slower                                                                                                   |
| xml_etree_process    | 57.9 ms                                                                                                           | 68.7 ms: 1.19x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.28 ms                                                                                                           | 9.70 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 49.9 ms                                                                                                           | 54.1 ms: 1.08x slower                                                                                                   |
| django_template | 35.7 ms                                                                                                           | 40.8 ms: 1.14x slower                                                                                                   |
| genshi_text     | 21.8 ms                                                                                                           | 26.0 ms: 1.19x slower                                                                                                   |
| mako            | 11.7 ms                                                                                                           | 16.0 ms: 1.37x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.19x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json | results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 279 ms                                                                                                            | 7.08 ms: 39.38x faster                                                                                                  |
| gc_traversal               | 4.31 ms                                                                                                           | 1.92 ms: 2.25x faster                                                                                                   |
| create_gc_cycles           | 1.88 ms                                                                                                           | 1.49 ms: 1.26x faster                                                                                                   |
| sqlite_synth               | 2.25 us                                                                                                           | 2.07 us: 1.09x faster                                                                                                   |
| asyncio_websockets         | 544 ms                                                                                                            | 511 ms: 1.07x faster                                                                                                    |
| regex_v8                   | 22.4 ms                                                                                                           | 21.2 ms: 1.06x faster                                                                                                   |
| pidigits                   | 202 ms                                                                                                            | 202 ms: 1.00x slower                                                                                                    |
| xml_etree_parse            | 131 ms                                                                                                            | 131 ms: 1.00x slower                                                                                                    |
| regex_dna                  | 173 ms                                                                                                            | 175 ms: 1.01x slower                                                                                                    |
| dulwich_log                | 69.0 ms                                                                                                           | 69.9 ms: 1.01x slower                                                                                                   |
| pathlib                    | 17.5 ms                                                                                                           | 17.8 ms: 1.02x slower                                                                                                   |
| regex_effbot               | 2.75 ms                                                                                                           | 2.80 ms: 1.02x slower                                                                                                   |
| logging_silent             | 102 ns                                                                                                            | 104 ns: 1.02x slower                                                                                                    |
| float                      | 70.9 ms                                                                                                           | 73.5 ms: 1.04x slower                                                                                                   |
| xml_etree_iterparse        | 84.4 ms                                                                                                           | 87.9 ms: 1.04x slower                                                                                                   |
| pycparser                  | 1.08 sec                                                                                                          | 1.14 sec: 1.05x slower                                                                                                  |
| bpe_tokeniser              | 4.22 sec                                                                                                          | 4.45 sec: 1.06x slower                                                                                                  |
| pylint                     | 283 ms                                                                                                            | 303 ms: 1.07x slower                                                                                                    |
| async_tree_io_tg           | 564 ms                                                                                                            | 603 ms: 1.07x slower                                                                                                    |
| docutils                   | 2.56 sec                                                                                                          | 2.75 sec: 1.07x slower                                                                                                  |
| pickle_pure_python         | 309 us                                                                                                            | 334 us: 1.08x slower                                                                                                    |
| many_optionals             | 940 us                                                                                                            | 1.02 ms: 1.08x slower                                                                                                   |
| genshi_xml                 | 49.9 ms                                                                                                           | 54.1 ms: 1.08x slower                                                                                                   |
| tomli_loads                | 1.82 sec                                                                                                          | 1.98 sec: 1.09x slower                                                                                                  |
| json                       | 5.04 ms                                                                                                           | 5.47 ms: 1.09x slower                                                                                                   |
| async_tree_none_tg         | 246 ms                                                                                                            | 267 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                                                            | 537 ms: 1.09x slower                                                                                                    |
| sphinx                     | 963 ms                                                                                                            | 1.05 sec: 1.09x slower                                                                                                  |
| deepcopy_reduce            | 2.63 us                                                                                                           | 2.88 us: 1.09x slower                                                                                                   |
| async_generators           | 341 ms                                                                                                            | 373 ms: 1.09x slower                                                                                                    |
| sympy_expand               | 469 ms                                                                                                            | 516 ms: 1.10x slower                                                                                                    |
| telco                      | 158 ms                                                                                                            | 174 ms: 1.10x slower                                                                                                    |
| pprint_safe_repr           | 700 ms                                                                                                            | 770 ms: 1.10x slower                                                                                                    |
| subparsers                 | 9.33 ms                                                                                                           | 10.3 ms: 1.10x slower                                                                                                   |
| bench_thread_pool          | 1.32 ms                                                                                                           | 1.46 ms: 1.11x slower                                                                                                   |
| deltablue                  | 3.29 ms                                                                                                           | 3.64 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python       | 213 us                                                                                                            | 236 us: 1.11x slower                                                                                                    |
| html5lib                   | 59.7 ms                                                                                                           | 66.3 ms: 1.11x slower                                                                                                   |
| sympy_str                  | 277 ms                                                                                                            | 307 ms: 1.11x slower                                                                                                    |
| sympy_sum                  | 157 ms                                                                                                            | 175 ms: 1.11x slower                                                                                                    |
| pprint_pformat             | 1.43 sec                                                                                                          | 1.59 sec: 1.11x slower                                                                                                  |
| hexiom                     | 5.76 ms                                                                                                           | 6.46 ms: 1.12x slower                                                                                                   |
| deepcopy                   | 238 us                                                                                                            | 267 us: 1.12x slower                                                                                                    |
| nqueens                    | 79.3 ms                                                                                                           | 89.4 ms: 1.13x slower                                                                                                   |
| async_tree_memoization_tg  | 293 ms                                                                                                            | 331 ms: 1.13x slower                                                                                                    |
| comprehensions             | 16.1 us                                                                                                           | 18.2 us: 1.13x slower                                                                                                   |
| 2to3                       | 248 ms                                                                                                            | 280 ms: 1.13x slower                                                                                                    |
| scimark_sor                | 108 ms                                                                                                            | 122 ms: 1.13x slower                                                                                                    |
| chaos                      | 55.8 ms                                                                                                           | 63.2 ms: 1.13x slower                                                                                                   |
| async_tree_io              | 552 ms                                                                                                            | 627 ms: 1.14x slower                                                                                                    |
| regex_compile              | 123 ms                                                                                                            | 140 ms: 1.14x slower                                                                                                    |
| json_dumps                 | 9.73 ms                                                                                                           | 11.1 ms: 1.14x slower                                                                                                   |
| sympy_integrate            | 19.0 ms                                                                                                           | 21.7 ms: 1.14x slower                                                                                                   |
| go                         | 105 ms                                                                                                            | 120 ms: 1.14x slower                                                                                                    |
| django_template            | 35.7 ms                                                                                                           | 40.8 ms: 1.14x slower                                                                                                   |
| pyflate                    | 413 ms                                                                                                            | 472 ms: 1.14x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                            | 561 ms: 1.14x slower                                                                                                    |
| mdp                        | 1.16 sec                                                                                                          | 1.32 sec: 1.15x slower                                                                                                  |
| json_loads                 | 28.1 us                                                                                                           | 32.4 us: 1.15x slower                                                                                                   |
| sqlglot_v2_optimize        | 50.9 ms                                                                                                           | 58.7 ms: 1.15x slower                                                                                                   |
| deepcopy_memo              | 26.5 us                                                                                                           | 30.6 us: 1.15x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                           | 1.75 ms: 1.16x slower                                                                                                   |
| scimark_fft                | 306 ms                                                                                                            | 355 ms: 1.16x slower                                                                                                    |
| sqlglot_v2_normalize       | 101 ms                                                                                                            | 117 ms: 1.16x slower                                                                                                    |
| thrift                     | 760 us                                                                                                            | 885 us: 1.16x slower                                                                                                    |
| scimark_lu                 | 109 ms                                                                                                            | 128 ms: 1.17x slower                                                                                                    |
| spectral_norm              | 95.5 ms                                                                                                           | 112 ms: 1.17x slower                                                                                                    |
| generators                 | 27.6 ms                                                                                                           | 32.4 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 82.1 ms                                                                                                           | 96.2 ms: 1.17x slower                                                                                                   |
| async_tree_none            | 244 ms                                                                                                            | 287 ms: 1.17x slower                                                                                                    |
| sqlglot_v2_parse           | 1.22 ms                                                                                                           | 1.43 ms: 1.18x slower                                                                                                   |
| logging_simple             | 5.89 us                                                                                                           | 6.95 us: 1.18x slower                                                                                                   |
| async_tree_memoization     | 302 ms                                                                                                            | 359 ms: 1.19x slower                                                                                                    |
| xml_etree_process          | 57.9 ms                                                                                                           | 68.7 ms: 1.19x slower                                                                                                   |
| k_core                     | 1.86 sec                                                                                                          | 2.21 sec: 1.19x slower                                                                                                  |
| genshi_text                | 21.8 ms                                                                                                           | 26.0 ms: 1.19x slower                                                                                                   |
| raytrace                   | 250 ms                                                                                                            | 302 ms: 1.20x slower                                                                                                    |
| fannkuch                   | 383 ms                                                                                                            | 462 ms: 1.21x slower                                                                                                    |
| logging_format             | 6.56 us                                                                                                           | 7.99 us: 1.22x slower                                                                                                   |
| richards_super             | 48.4 ms                                                                                                           | 59.4 ms: 1.23x slower                                                                                                   |
| meteor_contest             | 101 ms                                                                                                            | 124 ms: 1.23x slower                                                                                                    |
| typing_runtime_protocols   | 156 us                                                                                                            | 192 us: 1.23x slower                                                                                                    |
| shortest_path              | 430 ms                                                                                                            | 533 ms: 1.24x slower                                                                                                    |
| richards                   | 42.0 ms                                                                                                           | 52.2 ms: 1.24x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.44 ms                                                                                                           | 5.52 ms: 1.24x slower                                                                                                   |
| crypto_pyaes               | 69.4 ms                                                                                                           | 86.6 ms: 1.25x slower                                                                                                   |
| scimark_monte_carlo        | 62.5 ms                                                                                                           | 78.4 ms: 1.25x slower                                                                                                   |
| python_startup             | 12.5 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| connected_components       | 386 ms                                                                                                            | 492 ms: 1.27x slower                                                                                                    |
| python_startup_no_site     | 7.28 ms                                                                                                           | 9.70 ms: 1.33x slower                                                                                                   |
| mako                       | 11.7 ms                                                                                                           | 16.0 ms: 1.37x slower                                                                                                   |
| coverage                   | 81.1 ms                                                                                                           | 112 ms: 1.38x slower                                                                                                    |
| nbody                      | 90.8 ms                                                                                                           | 127 ms: 1.40x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): coroutines

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x