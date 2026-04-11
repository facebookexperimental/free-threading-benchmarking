# Results vs. base

- fork: python
- ref: dd88e77fad887aaf00ea
- machine: linux-x86_64
- commit hash: dd88e77
- commit date: 2026-04-10
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                            | 284 ms: 1.11x slower                                                                                                    |
| docutils       | 2.45 sec                                                                                                          | 2.62 sec: 1.07x slower                                                                                                  |
| html5lib       | 59.9 ms                                                                                                           | 66.1 ms: 1.10x slower                                                                                                   |
| sphinx         | 973 ms                                                                                                            | 1.06 sec: 1.09x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 543 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| coroutines                 | 23.8 ms                                                                                                           | 24.0 ms: 1.01x slower                                                                                                   |
| async_tree_io_tg           | 597 ms                                                                                                            | 611 ms: 1.02x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                                                            | 513 ms: 1.04x slower                                                                                                    |
| async_tree_none_tg         | 254 ms                                                                                                            | 263 ms: 1.04x slower                                                                                                    |
| async_tree_memoization_tg  | 308 ms                                                                                                            | 328 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                            | 537 ms: 1.07x slower                                                                                                    |
| async_generators           | 344 ms                                                                                                            | 375 ms: 1.09x slower                                                                                                    |
| async_tree_io              | 590 ms                                                                                                            | 645 ms: 1.09x slower                                                                                                    |
| async_tree_memoization     | 321 ms                                                                                                            | 355 ms: 1.10x slower                                                                                                    |
| async_tree_none            | 249 ms                                                                                                            | 294 ms: 1.18x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                            | 180 ms: 1.02x faster                                                                                                    |
| float          | 70.8 ms                                                                                                           | 73.8 ms: 1.04x slower                                                                                                   |
| nbody          | 96.9 ms                                                                                                           | 123 ms: 1.27x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 189 ms                                                                                                            | 176 ms: 1.08x faster                                                                                                    |
| regex_effbot   | 2.92 ms                                                                                                           | 2.71 ms: 1.08x faster                                                                                                   |
| regex_v8       | 21.9 ms                                                                                                           | 21.1 ms: 1.04x faster                                                                                                   |
| regex_compile  | 124 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.7 ms                                                                                                           | 87.5 ms: 1.03x slower                                                                                                   |
| tomli_loads          | 1.83 sec                                                                                                          | 1.96 sec: 1.07x slower                                                                                                  |
| json_loads           | 27.2 us                                                                                                           | 29.3 us: 1.08x slower                                                                                                   |
| pickle_pure_python   | 317 us                                                                                                            | 342 us: 1.08x slower                                                                                                    |
| json_dumps           | 9.66 ms                                                                                                           | 10.7 ms: 1.10x slower                                                                                                   |
| unpickle_pure_python | 215 us                                                                                                            | 241 us: 1.12x slower                                                                                                    |
| xml_etree_generate   | 84.5 ms                                                                                                           | 96.3 ms: 1.14x slower                                                                                                   |
| xml_etree_process    | 59.8 ms                                                                                                           | 69.0 ms: 1.15x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                                                           | 16.2 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.46 ms                                                                                                           | 9.88 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 49.9 ms                                                                                                           | 53.8 ms: 1.08x slower                                                                                                   |
| django_template | 36.0 ms                                                                                                           | 39.9 ms: 1.11x slower                                                                                                   |
| genshi_text     | 21.3 ms                                                                                                           | 25.5 ms: 1.20x slower                                                                                                   |
| mako            | 12.2 ms                                                                                                           | 16.0 ms: 1.31x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.17x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json | results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 303 ms                                                                                                            | 7.03 ms: 43.09x faster                                                                                                  |
| gc_traversal               | 4.36 ms                                                                                                           | 1.97 ms: 2.21x faster                                                                                                   |
| create_gc_cycles           | 1.92 ms                                                                                                           | 1.53 ms: 1.26x faster                                                                                                   |
| sqlite_synth               | 2.21 us                                                                                                           | 1.93 us: 1.15x faster                                                                                                   |
| regex_dna                  | 189 ms                                                                                                            | 176 ms: 1.08x faster                                                                                                    |
| regex_effbot               | 2.92 ms                                                                                                           | 2.71 ms: 1.08x faster                                                                                                   |
| asyncio_websockets         | 543 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| regex_v8                   | 21.9 ms                                                                                                           | 21.1 ms: 1.04x faster                                                                                                   |
| pidigits                   | 184 ms                                                                                                            | 180 ms: 1.02x faster                                                                                                    |
| coroutines                 | 23.8 ms                                                                                                           | 24.0 ms: 1.01x slower                                                                                                   |
| pathlib                    | 17.3 ms                                                                                                           | 17.6 ms: 1.02x slower                                                                                                   |
| async_tree_io_tg           | 597 ms                                                                                                            | 611 ms: 1.02x slower                                                                                                    |
| json                       | 4.99 ms                                                                                                           | 5.11 ms: 1.02x slower                                                                                                   |
| dulwich_log                | 68.8 ms                                                                                                           | 70.5 ms: 1.02x slower                                                                                                   |
| xml_etree_iterparse        | 84.7 ms                                                                                                           | 87.5 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                                                            | 513 ms: 1.04x slower                                                                                                    |
| async_tree_none_tg         | 254 ms                                                                                                            | 263 ms: 1.04x slower                                                                                                    |
| float                      | 70.8 ms                                                                                                           | 73.8 ms: 1.04x slower                                                                                                   |
| pylint                     | 284 ms                                                                                                            | 298 ms: 1.05x slower                                                                                                    |
| logging_silent             | 99.7 ns                                                                                                           | 105 ns: 1.05x slower                                                                                                    |
| bpe_tokeniser              | 4.15 sec                                                                                                          | 4.37 sec: 1.05x slower                                                                                                  |
| docutils                   | 2.45 sec                                                                                                          | 2.62 sec: 1.07x slower                                                                                                  |
| async_tree_memoization_tg  | 308 ms                                                                                                            | 328 ms: 1.07x slower                                                                                                    |
| many_optionals             | 946 us                                                                                                            | 1.01 ms: 1.07x slower                                                                                                   |
| tomli_loads                | 1.83 sec                                                                                                          | 1.96 sec: 1.07x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                            | 537 ms: 1.07x slower                                                                                                    |
| deltablue                  | 3.30 ms                                                                                                           | 3.54 ms: 1.07x slower                                                                                                   |
| json_loads                 | 27.2 us                                                                                                           | 29.3 us: 1.08x slower                                                                                                   |
| genshi_xml                 | 49.9 ms                                                                                                           | 53.8 ms: 1.08x slower                                                                                                   |
| pickle_pure_python         | 317 us                                                                                                            | 342 us: 1.08x slower                                                                                                    |
| telco                      | 158 ms                                                                                                            | 171 ms: 1.08x slower                                                                                                    |
| sympy_expand               | 485 ms                                                                                                            | 526 ms: 1.08x slower                                                                                                    |
| sphinx                     | 973 ms                                                                                                            | 1.06 sec: 1.09x slower                                                                                                  |
| async_generators           | 344 ms                                                                                                            | 375 ms: 1.09x slower                                                                                                    |
| async_tree_io              | 590 ms                                                                                                            | 645 ms: 1.09x slower                                                                                                    |
| bench_thread_pool          | 1.33 ms                                                                                                           | 1.46 ms: 1.10x slower                                                                                                   |
| comprehensions             | 16.3 us                                                                                                           | 17.9 us: 1.10x slower                                                                                                   |
| html5lib                   | 59.9 ms                                                                                                           | 66.1 ms: 1.10x slower                                                                                                   |
| generators                 | 29.3 ms                                                                                                           | 32.3 ms: 1.10x slower                                                                                                   |
| json_dumps                 | 9.66 ms                                                                                                           | 10.7 ms: 1.10x slower                                                                                                   |
| async_tree_memoization     | 321 ms                                                                                                            | 355 ms: 1.10x slower                                                                                                    |
| scimark_sor                | 111 ms                                                                                                            | 122 ms: 1.10x slower                                                                                                    |
| pprint_safe_repr           | 724 ms                                                                                                            | 800 ms: 1.11x slower                                                                                                    |
| 2to3                       | 257 ms                                                                                                            | 284 ms: 1.11x slower                                                                                                    |
| subparsers                 | 9.30 ms                                                                                                           | 10.3 ms: 1.11x slower                                                                                                   |
| django_template            | 36.0 ms                                                                                                           | 39.9 ms: 1.11x slower                                                                                                   |
| sqlglot_v2_optimize        | 51.3 ms                                                                                                           | 56.8 ms: 1.11x slower                                                                                                   |
| scimark_fft                | 317 ms                                                                                                            | 353 ms: 1.11x slower                                                                                                    |
| sqlglot_v2_normalize       | 103 ms                                                                                                            | 115 ms: 1.11x slower                                                                                                    |
| unpickle_pure_python       | 215 us                                                                                                            | 241 us: 1.12x slower                                                                                                    |
| pyflate                    | 414 ms                                                                                                            | 463 ms: 1.12x slower                                                                                                    |
| pprint_pformat             | 1.47 sec                                                                                                          | 1.65 sec: 1.12x slower                                                                                                  |
| deepcopy_reduce            | 2.61 us                                                                                                           | 2.94 us: 1.12x slower                                                                                                   |
| sympy_str                  | 278 ms                                                                                                            | 313 ms: 1.13x slower                                                                                                    |
| deepcopy                   | 238 us                                                                                                            | 269 us: 1.13x slower                                                                                                    |
| sympy_sum                  | 158 ms                                                                                                            | 179 ms: 1.13x slower                                                                                                    |
| xml_etree_generate         | 84.5 ms                                                                                                           | 96.3 ms: 1.14x slower                                                                                                   |
| scimark_lu                 | 112 ms                                                                                                            | 127 ms: 1.14x slower                                                                                                    |
| hexiom                     | 5.78 ms                                                                                                           | 6.59 ms: 1.14x slower                                                                                                   |
| sympy_integrate            | 19.2 ms                                                                                                           | 21.9 ms: 1.14x slower                                                                                                   |
| regex_compile              | 124 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| chaos                      | 54.4 ms                                                                                                           | 62.3 ms: 1.14x slower                                                                                                   |
| xml_etree_process          | 59.8 ms                                                                                                           | 69.0 ms: 1.15x slower                                                                                                   |
| fannkuch                   | 391 ms                                                                                                            | 452 ms: 1.16x slower                                                                                                    |
| nqueens                    | 75.4 ms                                                                                                           | 87.5 ms: 1.16x slower                                                                                                   |
| spectral_norm              | 94.6 ms                                                                                                           | 110 ms: 1.16x slower                                                                                                    |
| logging_simple             | 5.87 us                                                                                                           | 6.82 us: 1.16x slower                                                                                                   |
| go                         | 105 ms                                                                                                            | 122 ms: 1.16x slower                                                                                                    |
| deepcopy_memo              | 27.5 us                                                                                                           | 32.0 us: 1.16x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                           | 1.71 ms: 1.17x slower                                                                                                   |
| sqlglot_v2_parse           | 1.17 ms                                                                                                           | 1.37 ms: 1.17x slower                                                                                                   |
| async_tree_none            | 249 ms                                                                                                            | 294 ms: 1.18x slower                                                                                                    |
| thrift                     | 773 us                                                                                                            | 912 us: 1.18x slower                                                                                                    |
| k_core                     | 1.88 sec                                                                                                          | 2.22 sec: 1.18x slower                                                                                                  |
| logging_format             | 6.57 us                                                                                                           | 7.77 us: 1.18x slower                                                                                                   |
| raytrace                   | 254 ms                                                                                                            | 304 ms: 1.19x slower                                                                                                    |
| genshi_text                | 21.3 ms                                                                                                           | 25.5 ms: 1.20x slower                                                                                                   |
| typing_runtime_protocols   | 159 us                                                                                                            | 192 us: 1.21x slower                                                                                                    |
| shortest_path              | 435 ms                                                                                                            | 532 ms: 1.22x slower                                                                                                    |
| meteor_contest             | 101 ms                                                                                                            | 123 ms: 1.22x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.55 ms                                                                                                           | 5.59 ms: 1.23x slower                                                                                                   |
| richards_super             | 49.4 ms                                                                                                           | 60.7 ms: 1.23x slower                                                                                                   |
| connected_components       | 393 ms                                                                                                            | 484 ms: 1.23x slower                                                                                                    |
| richards                   | 43.0 ms                                                                                                           | 53.1 ms: 1.23x slower                                                                                                   |
| crypto_pyaes               | 70.4 ms                                                                                                           | 87.6 ms: 1.24x slower                                                                                                   |
| scimark_monte_carlo        | 63.4 ms                                                                                                           | 79.3 ms: 1.25x slower                                                                                                   |
| nbody                      | 96.9 ms                                                                                                           | 123 ms: 1.27x slower                                                                                                    |
| python_startup             | 12.7 ms                                                                                                           | 16.2 ms: 1.27x slower                                                                                                   |
| mako                       | 12.2 ms                                                                                                           | 16.0 ms: 1.31x slower                                                                                                   |
| python_startup_no_site     | 7.46 ms                                                                                                           | 9.88 ms: 1.32x slower                                                                                                   |
| coverage                   | 82.1 ms                                                                                                           | 110 ms: 1.34x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, pycparser

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.21x