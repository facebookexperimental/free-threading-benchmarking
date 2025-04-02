# Results vs. base

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.082x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 455 ms                                                                                                            | 512 ms: 1.12x slower                                                                                                    |
| docutils       | 3.68 sec                                                                                                          | 3.98 sec: 1.08x slower                                                                                                  |
| sphinx         | 1.40 sec                                                                                                          | 1.62 sec: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 890 ms                                                                                                            | 704 ms: 1.27x faster                                                                                                    |
| async_tree_none_tg         | 384 ms                                                                                                            | 317 ms: 1.21x faster                                                                                                    |
| async_tree_io              | 883 ms                                                                                                            | 778 ms: 1.13x faster                                                                                                    |
| async_tree_memoization_tg  | 482 ms                                                                                                            | 433 ms: 1.11x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 674 ms                                                                                                            | 625 ms: 1.08x faster                                                                                                    |
| async_generators           | 535 ms                                                                                                            | 552 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 674 ms                                                                                                            | 706 ms: 1.05x slower                                                                                                    |
| async_tree_memoization     | 449 ms                                                                                                            | 494 ms: 1.10x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x faster                                                                                                            |

Benchmark hidden because not significant (3): coroutines, async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 237 ms                                                                                                            | 229 ms: 1.03x faster                                                                                                    |
| float          | 95.2 ms                                                                                                           | 103 ms: 1.09x slower                                                                                                    |
| nbody          | 128 ms                                                                                                            | 147 ms: 1.15x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                                                            | 267 ms: 1.06x faster                                                                                                    |
| regex_compile  | 169 ms                                                                                                            | 191 ms: 1.13x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 295 us                                                                                                            | 314 us: 1.06x slower                                                                                                    |
| xml_etree_generate   | 121 ms                                                                                                            | 131 ms: 1.08x slower                                                                                                    |
| json_dumps           | 16.4 ms                                                                                                           | 18.1 ms: 1.11x slower                                                                                                   |
| xml_etree_process    | 80.4 ms                                                                                                           | 91.2 ms: 1.13x slower                                                                                                   |
| tomli_loads          | 2.46 sec                                                                                                          | 2.82 sec: 1.15x slower                                                                                                  |
| json_loads           | 36.5 us                                                                                                           | 41.9 us: 1.15x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 29.8 ms                                                                                                           | 34.6 ms: 1.16x slower                                                                                                   |
| python_startup_no_site | 17.6 ms                                                                                                           | 24.6 ms: 1.40x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 31.6 ms                                                                                                           | 35.6 ms: 1.13x slower                                                                                                   |
| django_template | 43.0 ms                                                                                                           | 51.5 ms: 1.20x slower                                                                                                   |
| mako            | 16.5 ms                                                                                                           | 21.4 ms: 1.30x slower                                                                                                   |
| genshi_xml      | 65.2 ms                                                                                                           | 85.5 ms: 1.31x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.23x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.62 ms                                                                                                           | 3.65 ms: 2.09x faster                                                                                                   |
| create_gc_cycles           | 3.64 ms                                                                                                           | 2.54 ms: 1.44x faster                                                                                                   |
| async_tree_io_tg           | 890 ms                                                                                                            | 704 ms: 1.27x faster                                                                                                    |
| async_tree_none_tg         | 384 ms                                                                                                            | 317 ms: 1.21x faster                                                                                                    |
| bench_mp_pool              | 96.7 ms                                                                                                           | 84.2 ms: 1.15x faster                                                                                                   |
| async_tree_io              | 883 ms                                                                                                            | 778 ms: 1.13x faster                                                                                                    |
| async_tree_memoization_tg  | 482 ms                                                                                                            | 433 ms: 1.11x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 674 ms                                                                                                            | 625 ms: 1.08x faster                                                                                                    |
| regex_dna                  | 284 ms                                                                                                            | 267 ms: 1.06x faster                                                                                                    |
| pycparser                  | 1.59 sec                                                                                                          | 1.52 sec: 1.05x faster                                                                                                  |
| pidigits                   | 237 ms                                                                                                            | 229 ms: 1.03x faster                                                                                                    |
| async_generators           | 535 ms                                                                                                            | 552 ms: 1.03x slower                                                                                                    |
| generators                 | 43.0 ms                                                                                                           | 44.8 ms: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 674 ms                                                                                                            | 706 ms: 1.05x slower                                                                                                    |
| dulwich_log                | 86.0 ms                                                                                                           | 90.5 ms: 1.05x slower                                                                                                   |
| unpickle_pure_python       | 295 us                                                                                                            | 314 us: 1.06x slower                                                                                                    |
| sqlglot_v2_optimize        | 70.3 ms                                                                                                           | 74.9 ms: 1.07x slower                                                                                                   |
| nqueens                    | 112 ms                                                                                                            | 120 ms: 1.07x slower                                                                                                    |
| sqlglot_v2_normalize       | 143 ms                                                                                                            | 153 ms: 1.07x slower                                                                                                    |
| logging_silent             | 127 ns                                                                                                            | 137 ns: 1.07x slower                                                                                                    |
| scimark_sor                | 151 ms                                                                                                            | 163 ms: 1.08x slower                                                                                                    |
| pylint                     | 403 ms                                                                                                            | 435 ms: 1.08x slower                                                                                                    |
| xml_etree_generate         | 121 ms                                                                                                            | 131 ms: 1.08x slower                                                                                                    |
| docutils                   | 3.68 sec                                                                                                          | 3.98 sec: 1.08x slower                                                                                                  |
| pathlib                    | 28.2 ms                                                                                                           | 30.6 ms: 1.09x slower                                                                                                   |
| float                      | 95.2 ms                                                                                                           | 103 ms: 1.09x slower                                                                                                    |
| scimark_lu                 | 155 ms                                                                                                            | 169 ms: 1.09x slower                                                                                                    |
| logging_simple             | 8.37 us                                                                                                           | 9.17 us: 1.09x slower                                                                                                   |
| deepcopy_reduce            | 3.69 us                                                                                                           | 4.05 us: 1.10x slower                                                                                                   |
| crypto_pyaes               | 102 ms                                                                                                            | 112 ms: 1.10x slower                                                                                                    |
| scimark_fft                | 438 ms                                                                                                            | 481 ms: 1.10x slower                                                                                                    |
| async_tree_memoization     | 449 ms                                                                                                            | 494 ms: 1.10x slower                                                                                                    |
| deepcopy                   | 333 us                                                                                                            | 368 us: 1.10x slower                                                                                                    |
| json_dumps                 | 16.4 ms                                                                                                           | 18.1 ms: 1.11x slower                                                                                                   |
| k_core                     | 4.01 sec                                                                                                          | 4.46 sec: 1.11x slower                                                                                                  |
| logging_format             | 9.21 us                                                                                                           | 10.3 us: 1.12x slower                                                                                                   |
| 2to3                       | 455 ms                                                                                                            | 512 ms: 1.12x slower                                                                                                    |
| genshi_text                | 31.6 ms                                                                                                           | 35.6 ms: 1.13x slower                                                                                                   |
| meteor_contest             | 151 ms                                                                                                            | 170 ms: 1.13x slower                                                                                                    |
| hexiom                     | 8.37 ms                                                                                                           | 9.47 ms: 1.13x slower                                                                                                   |
| regex_compile              | 169 ms                                                                                                            | 191 ms: 1.13x slower                                                                                                    |
| pyflate                    | 605 ms                                                                                                            | 686 ms: 1.13x slower                                                                                                    |
| xml_etree_process          | 80.4 ms                                                                                                           | 91.2 ms: 1.13x slower                                                                                                   |
| pprint_safe_repr           | 905 ms                                                                                                            | 1.04 sec: 1.14x slower                                                                                                  |
| tomli_loads                | 2.46 sec                                                                                                          | 2.82 sec: 1.15x slower                                                                                                  |
| sqlglot_v2_transpile       | 2.13 ms                                                                                                           | 2.44 ms: 1.15x slower                                                                                                   |
| json_loads                 | 36.5 us                                                                                                           | 41.9 us: 1.15x slower                                                                                                   |
| nbody                      | 128 ms                                                                                                            | 147 ms: 1.15x slower                                                                                                    |
| bpe_tokeniser              | 5.97 sec                                                                                                          | 6.89 sec: 1.15x slower                                                                                                  |
| comprehensions             | 22.2 us                                                                                                           | 25.6 us: 1.16x slower                                                                                                   |
| sympy_sum                  | 207 ms                                                                                                            | 239 ms: 1.16x slower                                                                                                    |
| sphinx                     | 1.40 sec                                                                                                          | 1.62 sec: 1.16x slower                                                                                                  |
| python_startup             | 29.8 ms                                                                                                           | 34.6 ms: 1.16x slower                                                                                                   |
| many_optionals             | 1.28 ms                                                                                                           | 1.48 ms: 1.16x slower                                                                                                   |
| sqlglot_v2_parse           | 1.67 ms                                                                                                           | 1.95 ms: 1.17x slower                                                                                                   |
| sympy_expand               | 583 ms                                                                                                            | 682 ms: 1.17x slower                                                                                                    |
| richards                   | 61.7 ms                                                                                                           | 72.3 ms: 1.17x slower                                                                                                   |
| pprint_pformat             | 1.82 sec                                                                                                          | 2.14 sec: 1.17x slower                                                                                                  |
| shortest_path              | 867 ms                                                                                                            | 1.02 sec: 1.17x slower                                                                                                  |
| richards_super             | 64.4 ms                                                                                                           | 75.7 ms: 1.18x slower                                                                                                   |
| fannkuch                   | 511 ms                                                                                                            | 601 ms: 1.18x slower                                                                                                    |
| sympy_str                  | 367 ms                                                                                                            | 433 ms: 1.18x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.12 ms                                                                                                           | 7.28 ms: 1.19x slower                                                                                                   |
| go                         | 152 ms                                                                                                            | 180 ms: 1.19x slower                                                                                                    |
| connected_components       | 798 ms                                                                                                            | 953 ms: 1.19x slower                                                                                                    |
| django_template            | 43.0 ms                                                                                                           | 51.5 ms: 1.20x slower                                                                                                   |
| raytrace                   | 336 ms                                                                                                            | 404 ms: 1.20x slower                                                                                                    |
| scimark_monte_carlo        | 92.0 ms                                                                                                           | 112 ms: 1.22x slower                                                                                                    |
| sympy_integrate            | 27.9 ms                                                                                                           | 34.0 ms: 1.22x slower                                                                                                   |
| sqlalchemy_declarative     | 183 ms                                                                                                            | 223 ms: 1.22x slower                                                                                                    |
| mdp                        | 1.94 sec                                                                                                          | 2.38 sec: 1.22x slower                                                                                                  |
| chaos                      | 69.9 ms                                                                                                           | 86.8 ms: 1.24x slower                                                                                                   |
| deepcopy_memo              | 36.7 us                                                                                                           | 47.0 us: 1.28x slower                                                                                                   |
| mako                       | 16.5 ms                                                                                                           | 21.4 ms: 1.30x slower                                                                                                   |
| genshi_xml                 | 65.2 ms                                                                                                           | 85.5 ms: 1.31x slower                                                                                                   |
| deltablue                  | 4.42 ms                                                                                                           | 5.82 ms: 1.32x slower                                                                                                   |
| telco                      | 9.95 ms                                                                                                           | 13.1 ms: 1.32x slower                                                                                                   |
| subparsers                 | 29.7 ms                                                                                                           | 40.1 ms: 1.35x slower                                                                                                   |
| typing_runtime_protocols   | 207 us                                                                                                            | 282 us: 1.37x slower                                                                                                    |
| python_startup_no_site     | 17.6 ms                                                                                                           | 24.6 ms: 1.40x slower                                                                                                   |
| coverage                   | 107 ms                                                                                                            | 150 ms: 1.40x slower                                                                                                    |
| sqlalchemy_imperative      | 23.9 ms                                                                                                           | 33.8 ms: 1.41x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (12): regex_effbot, json, xml_etree_iterparse, regex_v8, coroutines, pickle_pure_python, bench_thread_pool, xml_etree_parse, sqlite_synth, async_tree_none, asyncio_websockets, spectral_norm
Ignored benchmarks (1) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: html5lib

- Geometric mean (including insignificant results): 1.082x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x