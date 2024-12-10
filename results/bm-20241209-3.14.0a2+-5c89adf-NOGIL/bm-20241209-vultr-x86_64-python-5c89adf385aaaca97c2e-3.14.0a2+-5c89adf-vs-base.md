# Results vs. base

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.265x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                            | 369 ms: 1.43x slower                                                                                                    |
| docutils       | 2.57 sec                                                                                                          | 3.08 sec: 1.20x slower                                                                                                  |
| sphinx         | 997 ms                                                                                                            | 1.19 sec: 1.19x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                                                            | 520 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 599 ms                                                                                                            | 614 ms: 1.02x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 603 ms                                                                                                            | 642 ms: 1.07x slower                                                                                                    |
| coroutines                 | 22.0 ms                                                                                                           | 24.5 ms: 1.11x slower                                                                                                   |
| async_generators           | 362 ms                                                                                                            | 457 ms: 1.26x slower                                                                                                    |
| async_tree_none_tg         | 275 ms                                                                                                            | 359 ms: 1.30x slower                                                                                                    |
| async_tree_io_tg           | 622 ms                                                                                                            | 829 ms: 1.33x slower                                                                                                    |
| async_tree_memoization_tg  | 334 ms                                                                                                            | 449 ms: 1.34x slower                                                                                                    |
| async_tree_memoization     | 341 ms                                                                                                            | 475 ms: 1.39x slower                                                                                                    |
| async_tree_none            | 275 ms                                                                                                            | 388 ms: 1.41x slower                                                                                                    |
| async_tree_io              | 602 ms                                                                                                            | 853 ms: 1.42x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.23x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 221 ms                                                                                                            | 181 ms: 1.22x faster                                                                                                    |
| nbody          | 96.1 ms                                                                                                           | 131 ms: 1.37x slower                                                                                                    |
| float          | 79.3 ms                                                                                                           | 140 ms: 1.77x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                                                           | 24.3 ms: 1.04x faster                                                                                                   |
| regex_dna      | 179 ms                                                                                                            | 176 ms: 1.01x faster                                                                                                    |
| regex_effbot   | 2.77 ms                                                                                                           | 2.73 ms: 1.01x faster                                                                                                   |
| regex_compile  | 131 ms                                                                                                            | 181 ms: 1.38x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 127 ms                                                                                                            | 131 ms: 1.03x slower                                                                                                    |
| json_loads           | 24.9 us                                                                                                           | 28.4 us: 1.14x slower                                                                                                   |
| xml_etree_generate   | 85.3 ms                                                                                                           | 98.2 ms: 1.15x slower                                                                                                   |
| json_dumps           | 11.5 ms                                                                                                           | 14.2 ms: 1.24x slower                                                                                                   |
| tomli_loads          | 2.09 sec                                                                                                          | 2.66 sec: 1.27x slower                                                                                                  |
| xml_etree_process    | 59.7 ms                                                                                                           | 78.7 ms: 1.32x slower                                                                                                   |
| unpickle_pure_python | 215 us                                                                                                            | 336 us: 1.56x slower                                                                                                    |
| pickle_pure_python   | 320 us                                                                                                            | 515 us: 1.61x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.24x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                                                           | 17.5 ms: 1.20x slower                                                                                                   |
| python_startup_no_site | 7.47 ms                                                                                                           | 10.2 ms: 1.37x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 50.4 ms                                                                                                           | 63.8 ms: 1.27x slower                                                                                                   |
| genshi_text     | 22.0 ms                                                                                                           | 31.7 ms: 1.44x slower                                                                                                   |
| django_template | 35.8 ms                                                                                                           | 52.1 ms: 1.45x slower                                                                                                   |
| mako            | 11.6 ms                                                                                                           | 17.8 ms: 1.53x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.42x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.02 ms                                                                                                           | 3.27 ms: 1.23x faster                                                                                                   |
| pidigits                   | 221 ms                                                                                                            | 181 ms: 1.22x faster                                                                                                    |
| regex_v8                   | 25.2 ms                                                                                                           | 24.3 ms: 1.04x faster                                                                                                   |
| regex_dna                  | 179 ms                                                                                                            | 176 ms: 1.01x faster                                                                                                    |
| regex_effbot               | 2.77 ms                                                                                                           | 2.73 ms: 1.01x faster                                                                                                   |
| asyncio_websockets         | 523 ms                                                                                                            | 520 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 599 ms                                                                                                            | 614 ms: 1.02x slower                                                                                                    |
| xml_etree_parse            | 127 ms                                                                                                            | 131 ms: 1.03x slower                                                                                                    |
| sqlite_synth               | 2.22 us                                                                                                           | 2.30 us: 1.04x slower                                                                                                   |
| create_gc_cycles           | 1.69 ms                                                                                                           | 1.79 ms: 1.06x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 603 ms                                                                                                            | 642 ms: 1.07x slower                                                                                                    |
| json                       | 4.68 ms                                                                                                           | 5.14 ms: 1.10x slower                                                                                                   |
| pathlib                    | 18.3 ms                                                                                                           | 20.3 ms: 1.11x slower                                                                                                   |
| coroutines                 | 22.0 ms                                                                                                           | 24.5 ms: 1.11x slower                                                                                                   |
| json_loads                 | 24.9 us                                                                                                           | 28.4 us: 1.14x slower                                                                                                   |
| xml_etree_generate         | 85.3 ms                                                                                                           | 98.2 ms: 1.15x slower                                                                                                   |
| bpe_tokeniser              | 4.32 sec                                                                                                          | 5.01 sec: 1.16x slower                                                                                                  |
| spectral_norm              | 107 ms                                                                                                            | 125 ms: 1.17x slower                                                                                                    |
| scimark_fft                | 349 ms                                                                                                            | 408 ms: 1.17x slower                                                                                                    |
| telco                      | 7.38 ms                                                                                                           | 8.65 ms: 1.17x slower                                                                                                   |
| mdp                        | 2.35 sec                                                                                                          | 2.80 sec: 1.19x slower                                                                                                  |
| sphinx                     | 997 ms                                                                                                            | 1.19 sec: 1.19x slower                                                                                                  |
| k_core                     | 2.02 sec                                                                                                          | 2.42 sec: 1.20x slower                                                                                                  |
| docutils                   | 2.57 sec                                                                                                          | 3.08 sec: 1.20x slower                                                                                                  |
| python_startup             | 14.6 ms                                                                                                           | 17.5 ms: 1.20x slower                                                                                                   |
| coverage                   | 79.4 ms                                                                                                           | 98.1 ms: 1.24x slower                                                                                                   |
| json_dumps                 | 11.5 ms                                                                                                           | 14.2 ms: 1.24x slower                                                                                                   |
| nqueens                    | 79.0 ms                                                                                                           | 97.7 ms: 1.24x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.76 ms                                                                                                           | 5.91 ms: 1.24x slower                                                                                                   |
| shortest_path              | 441 ms                                                                                                            | 552 ms: 1.25x slower                                                                                                    |
| many_optionals             | 1.03 ms                                                                                                           | 1.29 ms: 1.25x slower                                                                                                   |
| connected_components       | 399 ms                                                                                                            | 501 ms: 1.26x slower                                                                                                    |
| async_generators           | 362 ms                                                                                                            | 457 ms: 1.26x slower                                                                                                    |
| dulwich_log                | 76.0 ms                                                                                                           | 96.1 ms: 1.27x slower                                                                                                   |
| genshi_xml                 | 50.4 ms                                                                                                           | 63.8 ms: 1.27x slower                                                                                                   |
| bench_mp_pool              | 86.0 ms                                                                                                           | 109 ms: 1.27x slower                                                                                                    |
| sqlglot_normalize          | 109 ms                                                                                                            | 138 ms: 1.27x slower                                                                                                    |
| tomli_loads                | 2.09 sec                                                                                                          | 2.66 sec: 1.27x slower                                                                                                  |
| deepcopy                   | 262 us                                                                                                            | 333 us: 1.27x slower                                                                                                    |
| typing_runtime_protocols   | 158 us                                                                                                            | 202 us: 1.28x slower                                                                                                    |
| sqlglot_optimize           | 54.1 ms                                                                                                           | 69.3 ms: 1.28x slower                                                                                                   |
| async_tree_none_tg         | 275 ms                                                                                                            | 359 ms: 1.30x slower                                                                                                    |
| meteor_contest             | 99.3 ms                                                                                                           | 131 ms: 1.32x slower                                                                                                    |
| xml_etree_process          | 59.7 ms                                                                                                           | 78.7 ms: 1.32x slower                                                                                                   |
| deepcopy_reduce            | 2.68 us                                                                                                           | 3.56 us: 1.33x slower                                                                                                   |
| deepcopy_memo              | 30.1 us                                                                                                           | 40.1 us: 1.33x slower                                                                                                   |
| async_tree_io_tg           | 622 ms                                                                                                            | 829 ms: 1.33x slower                                                                                                    |
| fannkuch                   | 370 ms                                                                                                            | 494 ms: 1.34x slower                                                                                                    |
| async_tree_memoization_tg  | 334 ms                                                                                                            | 449 ms: 1.34x slower                                                                                                    |
| generators                 | 29.0 ms                                                                                                           | 39.1 ms: 1.35x slower                                                                                                   |
| nbody                      | 96.1 ms                                                                                                           | 131 ms: 1.37x slower                                                                                                    |
| pylint                     | 280 ms                                                                                                            | 383 ms: 1.37x slower                                                                                                    |
| pprint_safe_repr           | 716 ms                                                                                                            | 981 ms: 1.37x slower                                                                                                    |
| python_startup_no_site     | 7.47 ms                                                                                                           | 10.2 ms: 1.37x slower                                                                                                   |
| pycparser                  | 1.12 sec                                                                                                          | 1.55 sec: 1.37x slower                                                                                                  |
| regex_compile              | 131 ms                                                                                                            | 181 ms: 1.38x slower                                                                                                    |
| crypto_pyaes               | 66.5 ms                                                                                                           | 92.0 ms: 1.38x slower                                                                                                   |
| pprint_pformat             | 1.46 sec                                                                                                          | 2.03 sec: 1.38x slower                                                                                                  |
| async_tree_memoization     | 341 ms                                                                                                            | 475 ms: 1.39x slower                                                                                                    |
| async_tree_none            | 275 ms                                                                                                            | 388 ms: 1.41x slower                                                                                                    |
| subparsers                 | 22.5 ms                                                                                                           | 31.9 ms: 1.41x slower                                                                                                   |
| async_tree_io              | 602 ms                                                                                                            | 853 ms: 1.42x slower                                                                                                    |
| 2to3                       | 259 ms                                                                                                            | 369 ms: 1.43x slower                                                                                                    |
| genshi_text                | 22.0 ms                                                                                                           | 31.7 ms: 1.44x slower                                                                                                   |
| django_template            | 35.8 ms                                                                                                           | 52.1 ms: 1.45x slower                                                                                                   |
| sympy_integrate            | 20.1 ms                                                                                                           | 29.6 ms: 1.47x slower                                                                                                   |
| mako                       | 11.6 ms                                                                                                           | 17.8 ms: 1.53x slower                                                                                                   |
| sqlalchemy_imperative      | 19.5 ms                                                                                                           | 30.0 ms: 1.54x slower                                                                                                   |
| comprehensions             | 17.5 us                                                                                                           | 27.2 us: 1.55x slower                                                                                                   |
| unpickle_pure_python       | 215 us                                                                                                            | 336 us: 1.56x slower                                                                                                    |
| thrift                     | 750 us                                                                                                            | 1.17 ms: 1.56x slower                                                                                                   |
| pyflate                    | 444 ms                                                                                                            | 695 ms: 1.57x slower                                                                                                    |
| sqlalchemy_declarative     | 128 ms                                                                                                            | 205 ms: 1.61x slower                                                                                                    |
| pickle_pure_python         | 320 us                                                                                                            | 515 us: 1.61x slower                                                                                                    |
| hexiom                     | 5.99 ms                                                                                                           | 9.85 ms: 1.64x slower                                                                                                   |
| scimark_lu                 | 112 ms                                                                                                            | 186 ms: 1.67x slower                                                                                                    |
| richards_super             | 52.9 ms                                                                                                           | 88.7 ms: 1.68x slower                                                                                                   |
| richards                   | 46.3 ms                                                                                                           | 78.8 ms: 1.70x slower                                                                                                   |
| sympy_str                  | 275 ms                                                                                                            | 476 ms: 1.73x slower                                                                                                    |
| logging_silent             | 108 ns                                                                                                            | 188 ns: 1.74x slower                                                                                                    |
| logging_format             | 6.79 us                                                                                                           | 12.0 us: 1.76x slower                                                                                                   |
| float                      | 79.3 ms                                                                                                           | 140 ms: 1.77x slower                                                                                                    |
| scimark_sor                | 135 ms                                                                                                            | 239 ms: 1.78x slower                                                                                                    |
| logging_simple             | 6.06 us                                                                                                           | 10.8 us: 1.78x slower                                                                                                   |
| chaos                      | 58.9 ms                                                                                                           | 107 ms: 1.81x slower                                                                                                    |
| sqlglot_transpile          | 1.60 ms                                                                                                           | 3.00 ms: 1.87x slower                                                                                                   |
| scimark_monte_carlo        | 65.2 ms                                                                                                           | 126 ms: 1.93x slower                                                                                                    |
| sqlglot_parse              | 1.29 ms                                                                                                           | 2.59 ms: 2.00x slower                                                                                                   |
| sympy_expand               | 461 ms                                                                                                            | 957 ms: 2.08x slower                                                                                                    |
| raytrace                   | 265 ms                                                                                                            | 565 ms: 2.13x slower                                                                                                    |
| sympy_sum                  | 153 ms                                                                                                            | 350 ms: 2.29x slower                                                                                                    |
| go                         | 120 ms                                                                                                            | 278 ms: 2.31x slower                                                                                                    |
| deltablue                  | 3.21 ms                                                                                                           | 8.28 ms: 2.58x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.43 ms: 3.32x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.38x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: html5lib

- Geometric mean (including insignificant results): 1.265x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x