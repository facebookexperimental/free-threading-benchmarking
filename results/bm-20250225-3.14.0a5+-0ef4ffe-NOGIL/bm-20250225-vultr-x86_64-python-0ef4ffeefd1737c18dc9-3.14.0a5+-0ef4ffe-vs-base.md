# Results vs. base

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.132x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                            | 303 ms: 1.21x slower                                                                                                    |
| docutils       | 2.54 sec                                                                                                          | 2.79 sec: 1.10x slower                                                                                                  |
| sphinx         | 971 ms                                                                                                            | 1.10 sec: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 597 ms                                                                                                            | 551 ms: 1.08x faster                                                                                                    |
| async_tree_none_tg         | 253 ms                                                                                                            | 236 ms: 1.07x faster                                                                                                    |
| async_tree_io              | 603 ms                                                                                                            | 583 ms: 1.03x faster                                                                                                    |
| asyncio_websockets         | 517 ms                                                                                                            | 511 ms: 1.01x faster                                                                                                    |
| async_tree_none            | 258 ms                                                                                                            | 274 ms: 1.06x slower                                                                                                    |
| coroutines                 | 21.4 ms                                                                                                           | 22.8 ms: 1.07x slower                                                                                                   |
| async_tree_memoization     | 312 ms                                                                                                            | 336 ms: 1.08x slower                                                                                                    |
| async_generators           | 318 ms                                                                                                            | 367 ms: 1.15x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                                                            | 570 ms: 1.21x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 482 ms                                                                                                            | 599 ms: 1.24x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 70.3 ms                                                                                                           | 76.4 ms: 1.09x slower                                                                                                   |
| pidigits       | 208 ms                                                                                                            | 244 ms: 1.18x slower                                                                                                    |
| nbody          | 86.9 ms                                                                                                           | 132 ms: 1.52x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                                                           | 23.4 ms: 1.06x faster                                                                                                   |
| regex_effbot   | 2.65 ms                                                                                                           | 2.78 ms: 1.05x slower                                                                                                   |
| regex_dna      | 171 ms                                                                                                            | 184 ms: 1.08x slower                                                                                                    |
| regex_compile  | 124 ms                                                                                                            | 155 ms: 1.24x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                                                           | 88.2 ms: 1.03x faster                                                                                                   |
| xml_etree_parse      | 129 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| json_loads           | 28.0 us                                                                                                           | 29.2 us: 1.04x slower                                                                                                   |
| json_dumps           | 11.1 ms                                                                                                           | 13.0 ms: 1.17x slower                                                                                                   |
| xml_etree_generate   | 82.0 ms                                                                                                           | 95.7 ms: 1.17x slower                                                                                                   |
| unpickle_pure_python | 211 us                                                                                                            | 247 us: 1.17x slower                                                                                                    |
| pickle_pure_python   | 307 us                                                                                                            | 360 us: 1.17x slower                                                                                                    |
| xml_etree_process    | 57.0 ms                                                                                                           | 69.5 ms: 1.22x slower                                                                                                   |
| tomli_loads          | 1.89 sec                                                                                                          | 2.36 sec: 1.25x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.6 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 7.51 ms                                                                                                           | 9.64 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.7 ms                                                                                                           | 59.6 ms: 1.25x slower                                                                                                   |
| django_template | 32.4 ms                                                                                                           | 42.2 ms: 1.30x slower                                                                                                   |
| mako            | 11.6 ms                                                                                                           | 15.7 ms: 1.36x slower                                                                                                   |
| genshi_text     | 20.4 ms                                                                                                           | 28.0 ms: 1.37x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.32x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.21 ms                                                                                                           | 1.72 ms: 2.45x faster                                                                                                   |
| sqlglot_normalize          | 280 ms                                                                                                            | 121 ms: 2.30x faster                                                                                                    |
| create_gc_cycles           | 1.81 ms                                                                                                           | 1.31 ms: 1.39x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.00 us: 1.10x faster                                                                                                   |
| async_tree_io_tg           | 597 ms                                                                                                            | 551 ms: 1.08x faster                                                                                                    |
| async_tree_none_tg         | 253 ms                                                                                                            | 236 ms: 1.07x faster                                                                                                    |
| regex_v8                   | 24.7 ms                                                                                                           | 23.4 ms: 1.06x faster                                                                                                   |
| async_tree_io              | 603 ms                                                                                                            | 583 ms: 1.03x faster                                                                                                    |
| xml_etree_iterparse        | 90.4 ms                                                                                                           | 88.2 ms: 1.03x faster                                                                                                   |
| asyncio_websockets         | 517 ms                                                                                                            | 511 ms: 1.01x faster                                                                                                    |
| xml_etree_parse            | 129 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| json                       | 4.99 ms                                                                                                           | 5.09 ms: 1.02x slower                                                                                                   |
| pathlib                    | 19.1 ms                                                                                                           | 19.6 ms: 1.03x slower                                                                                                   |
| json_loads                 | 28.0 us                                                                                                           | 29.2 us: 1.04x slower                                                                                                   |
| regex_effbot               | 2.65 ms                                                                                                           | 2.78 ms: 1.05x slower                                                                                                   |
| python_startup             | 14.7 ms                                                                                                           | 15.6 ms: 1.06x slower                                                                                                   |
| async_tree_none            | 258 ms                                                                                                            | 274 ms: 1.06x slower                                                                                                    |
| pycparser                  | 1.12 sec                                                                                                          | 1.19 sec: 1.06x slower                                                                                                  |
| coroutines                 | 21.4 ms                                                                                                           | 22.8 ms: 1.07x slower                                                                                                   |
| bench_mp_pool              | 88.3 ms                                                                                                           | 95.0 ms: 1.08x slower                                                                                                   |
| regex_dna                  | 171 ms                                                                                                            | 184 ms: 1.08x slower                                                                                                    |
| async_tree_memoization     | 312 ms                                                                                                            | 336 ms: 1.08x slower                                                                                                    |
| float                      | 70.3 ms                                                                                                           | 76.4 ms: 1.09x slower                                                                                                   |
| docutils                   | 2.54 sec                                                                                                          | 2.79 sec: 1.10x slower                                                                                                  |
| dulwich_log                | 75.0 ms                                                                                                           | 82.7 ms: 1.10x slower                                                                                                   |
| logging_silent             | 98.4 ns                                                                                                           | 109 ns: 1.11x slower                                                                                                    |
| sphinx                     | 971 ms                                                                                                            | 1.10 sec: 1.13x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                          | 2.30 sec: 1.13x slower                                                                                                  |
| bpe_tokeniser              | 4.15 sec                                                                                                          | 4.75 sec: 1.14x slower                                                                                                  |
| pylint                     | 274 ms                                                                                                            | 314 ms: 1.15x slower                                                                                                    |
| many_optionals             | 1.01 ms                                                                                                           | 1.17 ms: 1.15x slower                                                                                                   |
| async_generators           | 318 ms                                                                                                            | 367 ms: 1.15x slower                                                                                                    |
| mdp                        | 2.42 sec                                                                                                          | 2.79 sec: 1.16x slower                                                                                                  |
| subparsers                 | 21.7 ms                                                                                                           | 25.2 ms: 1.16x slower                                                                                                   |
| json_dumps                 | 11.1 ms                                                                                                           | 13.0 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 82.0 ms                                                                                                           | 95.7 ms: 1.17x slower                                                                                                   |
| unpickle_pure_python       | 211 us                                                                                                            | 247 us: 1.17x slower                                                                                                    |
| pickle_pure_python         | 307 us                                                                                                            | 360 us: 1.17x slower                                                                                                    |
| pidigits                   | 208 ms                                                                                                            | 244 ms: 1.18x slower                                                                                                    |
| sqlglot_optimize           | 51.0 ms                                                                                                           | 61.3 ms: 1.20x slower                                                                                                   |
| thrift                     | 726 us                                                                                                            | 873 us: 1.20x slower                                                                                                    |
| telco                      | 7.19 ms                                                                                                           | 8.67 ms: 1.21x slower                                                                                                   |
| sympy_expand               | 453 ms                                                                                                            | 546 ms: 1.21x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                                                            | 570 ms: 1.21x slower                                                                                                    |
| 2to3                       | 250 ms                                                                                                            | 303 ms: 1.21x slower                                                                                                    |
| coverage                   | 79.5 ms                                                                                                           | 96.5 ms: 1.21x slower                                                                                                   |
| scimark_sor                | 112 ms                                                                                                            | 136 ms: 1.21x slower                                                                                                    |
| generators                 | 26.7 ms                                                                                                           | 32.5 ms: 1.21x slower                                                                                                   |
| xml_etree_process          | 57.0 ms                                                                                                           | 69.5 ms: 1.22x slower                                                                                                   |
| raytrace                   | 257 ms                                                                                                            | 315 ms: 1.23x slower                                                                                                    |
| sqlalchemy_imperative      | 19.2 ms                                                                                                           | 23.6 ms: 1.23x slower                                                                                                   |
| pyflate                    | 402 ms                                                                                                            | 495 ms: 1.23x slower                                                                                                    |
| pprint_safe_repr           | 677 ms                                                                                                            | 835 ms: 1.23x slower                                                                                                    |
| sympy_sum                  | 151 ms                                                                                                            | 186 ms: 1.23x slower                                                                                                    |
| deepcopy_reduce            | 2.53 us                                                                                                           | 3.12 us: 1.23x slower                                                                                                   |
| go                         | 111 ms                                                                                                            | 138 ms: 1.24x slower                                                                                                    |
| sqlalchemy_declarative     | 126 ms                                                                                                            | 156 ms: 1.24x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 482 ms                                                                                                            | 599 ms: 1.24x slower                                                                                                    |
| pprint_pformat             | 1.39 sec                                                                                                          | 1.73 sec: 1.24x slower                                                                                                  |
| sympy_integrate            | 19.3 ms                                                                                                           | 24.0 ms: 1.24x slower                                                                                                   |
| regex_compile              | 124 ms                                                                                                            | 155 ms: 1.24x slower                                                                                                    |
| comprehensions             | 15.9 us                                                                                                           | 19.8 us: 1.24x slower                                                                                                   |
| logging_simple             | 5.82 us                                                                                                           | 7.25 us: 1.25x slower                                                                                                   |
| spectral_norm              | 90.5 ms                                                                                                           | 113 ms: 1.25x slower                                                                                                    |
| deltablue                  | 3.02 ms                                                                                                           | 3.77 ms: 1.25x slower                                                                                                   |
| tomli_loads                | 1.89 sec                                                                                                          | 2.36 sec: 1.25x slower                                                                                                  |
| genshi_xml                 | 47.7 ms                                                                                                           | 59.6 ms: 1.25x slower                                                                                                   |
| sympy_str                  | 267 ms                                                                                                            | 335 ms: 1.25x slower                                                                                                    |
| logging_format             | 6.63 us                                                                                                           | 8.33 us: 1.26x slower                                                                                                   |
| sqlglot_transpile          | 1.53 ms                                                                                                           | 1.92 ms: 1.26x slower                                                                                                   |
| chaos                      | 54.8 ms                                                                                                           | 69.1 ms: 1.26x slower                                                                                                   |
| scimark_lu                 | 111 ms                                                                                                            | 140 ms: 1.26x slower                                                                                                    |
| deepcopy                   | 245 us                                                                                                            | 310 us: 1.26x slower                                                                                                    |
| shortest_path              | 429 ms                                                                                                            | 544 ms: 1.27x slower                                                                                                    |
| connected_components       | 388 ms                                                                                                            | 494 ms: 1.27x slower                                                                                                    |
| scimark_fft                | 309 ms                                                                                                            | 397 ms: 1.28x slower                                                                                                    |
| python_startup_no_site     | 7.51 ms                                                                                                           | 9.64 ms: 1.28x slower                                                                                                   |
| crypto_pyaes               | 67.0 ms                                                                                                           | 86.6 ms: 1.29x slower                                                                                                   |
| sqlglot_parse              | 1.23 ms                                                                                                           | 1.60 ms: 1.30x slower                                                                                                   |
| hexiom                     | 5.67 ms                                                                                                           | 7.38 ms: 1.30x slower                                                                                                   |
| django_template            | 32.4 ms                                                                                                           | 42.2 ms: 1.30x slower                                                                                                   |
| nqueens                    | 74.7 ms                                                                                                           | 97.4 ms: 1.30x slower                                                                                                   |
| deepcopy_memo              | 29.1 us                                                                                                           | 37.9 us: 1.30x slower                                                                                                   |
| richards                   | 41.9 ms                                                                                                           | 54.7 ms: 1.31x slower                                                                                                   |
| meteor_contest             | 99.2 ms                                                                                                           | 131 ms: 1.32x slower                                                                                                    |
| typing_runtime_protocols   | 152 us                                                                                                            | 200 us: 1.32x slower                                                                                                    |
| scimark_monte_carlo        | 62.3 ms                                                                                                           | 82.4 ms: 1.32x slower                                                                                                   |
| richards_super             | 47.4 ms                                                                                                           | 63.4 ms: 1.34x slower                                                                                                   |
| fannkuch                   | 366 ms                                                                                                            | 497 ms: 1.36x slower                                                                                                    |
| mako                       | 11.6 ms                                                                                                           | 15.7 ms: 1.36x slower                                                                                                   |
| genshi_text                | 20.4 ms                                                                                                           | 28.0 ms: 1.37x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.15 ms                                                                                                           | 5.95 ms: 1.43x slower                                                                                                   |
| nbody                      | 86.9 ms                                                                                                           | 132 ms: 1.52x slower                                                                                                    |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.31 ms: 3.20x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: html5lib

- Geometric mean (including insignificant results): 1.132x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.20x