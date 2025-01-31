# Results vs. base

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.134x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                                                            | 304 ms: 1.20x slower                                                                                                    |
| docutils       | 2.54 sec                                                                                                          | 2.80 sec: 1.10x slower                                                                                                  |
| sphinx         | 972 ms                                                                                                            | 1.12 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 623 ms                                                                                                            | 579 ms: 1.08x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 538 ms                                                                                                            | 508 ms: 1.06x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 552 ms                                                                                                            | 538 ms: 1.03x faster                                                                                                    |
| async_tree_io              | 622 ms                                                                                                            | 607 ms: 1.02x faster                                                                                                    |
| asyncio_websockets         | 517 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                    |
| async_tree_memoization_tg  | 318 ms                                                                                                            | 322 ms: 1.01x slower                                                                                                    |
| coroutines                 | 21.9 ms                                                                                                           | 23.5 ms: 1.07x slower                                                                                                   |
| async_tree_none            | 268 ms                                                                                                            | 288 ms: 1.08x slower                                                                                                    |
| async_tree_memoization     | 323 ms                                                                                                            | 354 ms: 1.09x slower                                                                                                    |
| async_generators           | 321 ms                                                                                                            | 374 ms: 1.16x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 210 ms                                                                                                            | 201 ms: 1.04x faster                                                                                                    |
| float          | 70.8 ms                                                                                                           | 76.9 ms: 1.09x slower                                                                                                   |
| nbody          | 88.7 ms                                                                                                           | 134 ms: 1.51x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                                                           | 2.91 ms: 1.03x slower                                                                                                   |
| regex_v8       | 22.8 ms                                                                                                           | 23.7 ms: 1.04x slower                                                                                                   |
| regex_dna      | 171 ms                                                                                                            | 187 ms: 1.09x slower                                                                                                    |
| regex_compile  | 125 ms                                                                                                            | 150 ms: 1.20x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.4 ms                                                                                                           | 88.6 ms: 1.03x faster                                                                                                   |
| json_loads           | 28.5 us                                                                                                           | 31.4 us: 1.10x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 12.9 ms: 1.15x slower                                                                                                   |
| xml_etree_generate   | 83.5 ms                                                                                                           | 97.4 ms: 1.17x slower                                                                                                   |
| unpickle_pure_python | 209 us                                                                                                            | 247 us: 1.18x slower                                                                                                    |
| xml_etree_process    | 58.0 ms                                                                                                           | 69.1 ms: 1.19x slower                                                                                                   |
| pickle_pure_python   | 309 us                                                                                                            | 372 us: 1.20x slower                                                                                                    |
| tomli_loads          | 1.85 sec                                                                                                          | 2.29 sec: 1.24x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.4 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 7.47 ms                                                                                                           | 9.66 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.1 ms                                                                                                           | 59.8 ms: 1.24x slower                                                                                                   |
| django_template | 34.2 ms                                                                                                           | 42.6 ms: 1.25x slower                                                                                                   |
| genshi_text     | 20.7 ms                                                                                                           | 27.6 ms: 1.33x slower                                                                                                   |
| mako            | 11.6 ms                                                                                                           | 15.7 ms: 1.36x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.29x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                                                           | 1.68 ms: 2.54x faster                                                                                                   |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.41 ms: 1.30x faster                                                                                                   |
| async_tree_io_tg           | 623 ms                                                                                                            | 579 ms: 1.08x faster                                                                                                    |
| sqlite_synth               | 2.17 us                                                                                                           | 2.04 us: 1.07x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 538 ms                                                                                                            | 508 ms: 1.06x faster                                                                                                    |
| pidigits                   | 210 ms                                                                                                            | 201 ms: 1.04x faster                                                                                                    |
| xml_etree_iterparse        | 91.4 ms                                                                                                           | 88.6 ms: 1.03x faster                                                                                                   |
| async_tree_cpu_io_mixed    | 552 ms                                                                                                            | 538 ms: 1.03x faster                                                                                                    |
| async_tree_io              | 622 ms                                                                                                            | 607 ms: 1.02x faster                                                                                                    |
| asyncio_websockets         | 517 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                    |
| async_tree_memoization_tg  | 318 ms                                                                                                            | 322 ms: 1.01x slower                                                                                                    |
| regex_effbot               | 2.84 ms                                                                                                           | 2.91 ms: 1.03x slower                                                                                                   |
| regex_v8                   | 22.8 ms                                                                                                           | 23.7 ms: 1.04x slower                                                                                                   |
| pathlib                    | 18.0 ms                                                                                                           | 18.7 ms: 1.04x slower                                                                                                   |
| python_startup             | 14.7 ms                                                                                                           | 15.4 ms: 1.05x slower                                                                                                   |
| bench_mp_pool              | 88.0 ms                                                                                                           | 92.6 ms: 1.05x slower                                                                                                   |
| pycparser                  | 1.11 sec                                                                                                          | 1.18 sec: 1.06x slower                                                                                                  |
| coroutines                 | 21.9 ms                                                                                                           | 23.5 ms: 1.07x slower                                                                                                   |
| async_tree_none            | 268 ms                                                                                                            | 288 ms: 1.08x slower                                                                                                    |
| json                       | 5.03 ms                                                                                                           | 5.43 ms: 1.08x slower                                                                                                   |
| mdp                        | 2.45 sec                                                                                                          | 2.66 sec: 1.08x slower                                                                                                  |
| logging_silent             | 105 ns                                                                                                            | 113 ns: 1.08x slower                                                                                                    |
| float                      | 70.8 ms                                                                                                           | 76.9 ms: 1.09x slower                                                                                                   |
| regex_dna                  | 171 ms                                                                                                            | 187 ms: 1.09x slower                                                                                                    |
| dulwich_log                | 74.9 ms                                                                                                           | 81.9 ms: 1.09x slower                                                                                                   |
| async_tree_memoization     | 323 ms                                                                                                            | 354 ms: 1.09x slower                                                                                                    |
| docutils                   | 2.54 sec                                                                                                          | 2.80 sec: 1.10x slower                                                                                                  |
| json_loads                 | 28.5 us                                                                                                           | 31.4 us: 1.10x slower                                                                                                   |
| bpe_tokeniser              | 4.14 sec                                                                                                          | 4.65 sec: 1.12x slower                                                                                                  |
| k_core                     | 2.04 sec                                                                                                          | 2.32 sec: 1.13x slower                                                                                                  |
| pylint                     | 277 ms                                                                                                            | 317 ms: 1.14x slower                                                                                                    |
| json_dumps                 | 11.2 ms                                                                                                           | 12.9 ms: 1.15x slower                                                                                                   |
| sphinx                     | 972 ms                                                                                                            | 1.12 sec: 1.15x slower                                                                                                  |
| generators                 | 29.0 ms                                                                                                           | 33.5 ms: 1.16x slower                                                                                                   |
| async_generators           | 321 ms                                                                                                            | 374 ms: 1.16x slower                                                                                                    |
| many_optionals             | 1.01 ms                                                                                                           | 1.18 ms: 1.16x slower                                                                                                   |
| xml_etree_generate         | 83.5 ms                                                                                                           | 97.4 ms: 1.17x slower                                                                                                   |
| sqlglot_normalize          | 103 ms                                                                                                            | 120 ms: 1.17x slower                                                                                                    |
| pprint_safe_repr           | 698 ms                                                                                                            | 817 ms: 1.17x slower                                                                                                    |
| telco                      | 7.31 ms                                                                                                           | 8.57 ms: 1.17x slower                                                                                                   |
| scimark_sor                | 112 ms                                                                                                            | 132 ms: 1.17x slower                                                                                                    |
| pprint_pformat             | 1.43 sec                                                                                                          | 1.68 sec: 1.18x slower                                                                                                  |
| unpickle_pure_python       | 209 us                                                                                                            | 247 us: 1.18x slower                                                                                                    |
| sqlglot_optimize           | 51.4 ms                                                                                                           | 61.1 ms: 1.19x slower                                                                                                   |
| xml_etree_process          | 58.0 ms                                                                                                           | 69.1 ms: 1.19x slower                                                                                                   |
| subparsers                 | 21.6 ms                                                                                                           | 25.8 ms: 1.19x slower                                                                                                   |
| regex_compile              | 125 ms                                                                                                            | 150 ms: 1.20x slower                                                                                                    |
| pickle_pure_python         | 309 us                                                                                                            | 372 us: 1.20x slower                                                                                                    |
| 2to3                       | 253 ms                                                                                                            | 304 ms: 1.20x slower                                                                                                    |
| scimark_lu                 | 113 ms                                                                                                            | 136 ms: 1.21x slower                                                                                                    |
| sympy_expand               | 450 ms                                                                                                            | 545 ms: 1.21x slower                                                                                                    |
| coverage                   | 80.0 ms                                                                                                           | 97.3 ms: 1.22x slower                                                                                                   |
| spectral_norm              | 89.3 ms                                                                                                           | 109 ms: 1.22x slower                                                                                                    |
| scimark_fft                | 311 ms                                                                                                            | 380 ms: 1.22x slower                                                                                                    |
| comprehensions             | 16.4 us                                                                                                           | 20.0 us: 1.22x slower                                                                                                   |
| deepcopy_reduce            | 2.61 us                                                                                                           | 3.18 us: 1.22x slower                                                                                                   |
| pyflate                    | 407 ms                                                                                                            | 498 ms: 1.22x slower                                                                                                    |
| sympy_sum                  | 151 ms                                                                                                            | 185 ms: 1.22x slower                                                                                                    |
| deepcopy                   | 252 us                                                                                                            | 310 us: 1.23x slower                                                                                                    |
| sympy_integrate            | 19.6 ms                                                                                                           | 24.1 ms: 1.23x slower                                                                                                   |
| thrift                     | 731 us                                                                                                            | 902 us: 1.23x slower                                                                                                    |
| tomli_loads                | 1.85 sec                                                                                                          | 2.29 sec: 1.24x slower                                                                                                  |
| sympy_str                  | 269 ms                                                                                                            | 333 ms: 1.24x slower                                                                                                    |
| sqlalchemy_declarative     | 127 ms                                                                                                            | 157 ms: 1.24x slower                                                                                                    |
| go                         | 112 ms                                                                                                            | 139 ms: 1.24x slower                                                                                                    |
| chaos                      | 55.4 ms                                                                                                           | 68.8 ms: 1.24x slower                                                                                                   |
| genshi_xml                 | 48.1 ms                                                                                                           | 59.8 ms: 1.24x slower                                                                                                   |
| sqlglot_transpile          | 1.54 ms                                                                                                           | 1.91 ms: 1.24x slower                                                                                                   |
| logging_simple             | 5.89 us                                                                                                           | 7.35 us: 1.25x slower                                                                                                   |
| django_template            | 34.2 ms                                                                                                           | 42.6 ms: 1.25x slower                                                                                                   |
| nqueens                    | 76.9 ms                                                                                                           | 96.2 ms: 1.25x slower                                                                                                   |
| connected_components       | 394 ms                                                                                                            | 493 ms: 1.25x slower                                                                                                    |
| raytrace                   | 261 ms                                                                                                            | 327 ms: 1.25x slower                                                                                                    |
| sqlalchemy_imperative      | 19.1 ms                                                                                                           | 24.1 ms: 1.26x slower                                                                                                   |
| logging_format             | 6.55 us                                                                                                           | 8.30 us: 1.27x slower                                                                                                   |
| shortest_path              | 431 ms                                                                                                            | 547 ms: 1.27x slower                                                                                                    |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.59 ms: 1.28x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.29 ms                                                                                                           | 5.53 ms: 1.29x slower                                                                                                   |
| hexiom                     | 5.73 ms                                                                                                           | 7.40 ms: 1.29x slower                                                                                                   |
| deepcopy_memo              | 29.6 us                                                                                                           | 38.3 us: 1.29x slower                                                                                                   |
| python_startup_no_site     | 7.47 ms                                                                                                           | 9.66 ms: 1.29x slower                                                                                                   |
| typing_runtime_protocols   | 153 us                                                                                                            | 200 us: 1.31x slower                                                                                                    |
| meteor_contest             | 98.6 ms                                                                                                           | 131 ms: 1.32x slower                                                                                                    |
| genshi_text                | 20.7 ms                                                                                                           | 27.6 ms: 1.33x slower                                                                                                   |
| fannkuch                   | 364 ms                                                                                                            | 487 ms: 1.34x slower                                                                                                    |
| crypto_pyaes               | 65.7 ms                                                                                                           | 88.1 ms: 1.34x slower                                                                                                   |
| richards_super             | 48.2 ms                                                                                                           | 65.2 ms: 1.35x slower                                                                                                   |
| scimark_monte_carlo        | 60.9 ms                                                                                                           | 82.5 ms: 1.35x slower                                                                                                   |
| mako                       | 11.6 ms                                                                                                           | 15.7 ms: 1.36x slower                                                                                                   |
| richards                   | 41.7 ms                                                                                                           | 57.2 ms: 1.37x slower                                                                                                   |
| nbody                      | 88.7 ms                                                                                                           | 134 ms: 1.51x slower                                                                                                    |
| deltablue                  | 3.06 ms                                                                                                           | 4.67 ms: 1.52x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.32 ms: 3.23x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: html5lib

- Geometric mean (including insignificant results): 1.134x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x