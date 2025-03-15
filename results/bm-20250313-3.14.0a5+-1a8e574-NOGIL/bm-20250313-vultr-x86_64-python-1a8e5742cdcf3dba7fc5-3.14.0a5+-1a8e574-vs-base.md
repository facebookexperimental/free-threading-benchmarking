# Results vs. base

- fork: python
- ref: 1a8e5742cdcf3dba7fc5
- machine: linux-x86_64
- commit hash: 1a8e574
- commit date: 2025-03-13
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                                                            | 299 ms: 1.16x slower                                                                                                    |
| docutils       | 2.61 sec                                                                                                          | 2.80 sec: 1.07x slower                                                                                                  |
| sphinx         | 995 ms                                                                                                            | 1.10 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                                                            | 546 ms: 1.15x faster                                                                                                    |
| async_tree_none_tg         | 267 ms                                                                                                            | 236 ms: 1.13x faster                                                                                                    |
| async_tree_io              | 630 ms                                                                                                            | 583 ms: 1.08x faster                                                                                                    |
| async_tree_memoization_tg  | 318 ms                                                                                                            | 304 ms: 1.05x faster                                                                                                    |
| async_tree_memoization     | 329 ms                                                                                                            | 339 ms: 1.03x slower                                                                                                    |
| coroutines                 | 23.4 ms                                                                                                           | 24.1 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                                                            | 530 ms: 1.05x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 517 ms                                                                                                            | 561 ms: 1.09x slower                                                                                                    |
| async_generators           | 339 ms                                                                                                            | 376 ms: 1.11x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 75.8 ms                                                                                                           | 77.9 ms: 1.03x slower                                                                                                   |
| pidigits       | 187 ms                                                                                                            | 202 ms: 1.08x slower                                                                                                    |
| nbody          | 102 ms                                                                                                            | 134 ms: 1.31x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                                                           | 23.4 ms: 1.05x faster                                                                                                   |
| regex_effbot   | 2.77 ms                                                                                                           | 2.70 ms: 1.03x faster                                                                                                   |
| regex_dna      | 179 ms                                                                                                            | 184 ms: 1.03x slower                                                                                                    |
| regex_compile  | 130 ms                                                                                                            | 158 ms: 1.22x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.4 ms                                                                                                           | 87.7 ms: 1.07x faster                                                                                                   |
| xml_etree_parse      | 130 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| json_loads           | 27.0 us                                                                                                           | 29.2 us: 1.08x slower                                                                                                   |
| pickle_pure_python   | 324 us                                                                                                            | 360 us: 1.11x slower                                                                                                    |
| xml_etree_generate   | 86.5 ms                                                                                                           | 96.6 ms: 1.12x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 12.8 ms: 1.14x slower                                                                                                   |
| unpickle_pure_python | 224 us                                                                                                            | 257 us: 1.14x slower                                                                                                    |
| xml_etree_process    | 60.1 ms                                                                                                           | 70.4 ms: 1.17x slower                                                                                                   |
| tomli_loads          | 2.00 sec                                                                                                          | 2.38 sec: 1.19x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                                                           | 15.8 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 8.63 ms                                                                                                           | 11.2 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 37.2 ms                                                                                                           | 43.1 ms: 1.16x slower                                                                                                   |
| genshi_xml      | 51.0 ms                                                                                                           | 59.6 ms: 1.17x slower                                                                                                   |
| genshi_text     | 21.9 ms                                                                                                           | 28.1 ms: 1.28x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 15.9 ms: 1.32x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.23x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json | results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.76 ms                                                                                                           | 1.74 ms: 2.74x faster                                                                                                   |
| create_gc_cycles           | 1.83 ms                                                                                                           | 1.33 ms: 1.37x faster                                                                                                   |
| async_tree_io_tg           | 628 ms                                                                                                            | 546 ms: 1.15x faster                                                                                                    |
| async_tree_none_tg         | 267 ms                                                                                                            | 236 ms: 1.13x faster                                                                                                    |
| sqlite_synth               | 2.21 us                                                                                                           | 2.02 us: 1.09x faster                                                                                                   |
| async_tree_io              | 630 ms                                                                                                            | 583 ms: 1.08x faster                                                                                                    |
| xml_etree_iterparse        | 93.4 ms                                                                                                           | 87.7 ms: 1.07x faster                                                                                                   |
| regex_v8                   | 24.5 ms                                                                                                           | 23.4 ms: 1.05x faster                                                                                                   |
| async_tree_memoization_tg  | 318 ms                                                                                                            | 304 ms: 1.05x faster                                                                                                    |
| regex_effbot               | 2.77 ms                                                                                                           | 2.70 ms: 1.03x faster                                                                                                   |
| pathlib                    | 19.6 ms                                                                                                           | 19.3 ms: 1.01x faster                                                                                                   |
| xml_etree_parse            | 130 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| pycparser                  | 1.16 sec                                                                                                          | 1.19 sec: 1.02x slower                                                                                                  |
| regex_dna                  | 179 ms                                                                                                            | 184 ms: 1.03x slower                                                                                                    |
| float                      | 75.8 ms                                                                                                           | 77.9 ms: 1.03x slower                                                                                                   |
| async_tree_memoization     | 329 ms                                                                                                            | 339 ms: 1.03x slower                                                                                                    |
| coroutines                 | 23.4 ms                                                                                                           | 24.1 ms: 1.03x slower                                                                                                   |
| json                       | 4.89 ms                                                                                                           | 5.10 ms: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                                                            | 530 ms: 1.05x slower                                                                                                    |
| python_startup             | 14.9 ms                                                                                                           | 15.8 ms: 1.06x slower                                                                                                   |
| generators                 | 29.7 ms                                                                                                           | 31.6 ms: 1.06x slower                                                                                                   |
| docutils                   | 2.61 sec                                                                                                          | 2.80 sec: 1.07x slower                                                                                                  |
| pidigits                   | 187 ms                                                                                                            | 202 ms: 1.08x slower                                                                                                    |
| dulwich_log                | 67.5 ms                                                                                                           | 73.0 ms: 1.08x slower                                                                                                   |
| json_loads                 | 27.0 us                                                                                                           | 29.2 us: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 517 ms                                                                                                            | 561 ms: 1.09x slower                                                                                                    |
| bench_mp_pool              | 88.2 ms                                                                                                           | 95.9 ms: 1.09x slower                                                                                                   |
| bpe_tokeniser              | 4.43 sec                                                                                                          | 4.84 sec: 1.09x slower                                                                                                  |
| sphinx                     | 995 ms                                                                                                            | 1.10 sec: 1.10x slower                                                                                                  |
| pylint                     | 285 ms                                                                                                            | 315 ms: 1.10x slower                                                                                                    |
| async_generators           | 339 ms                                                                                                            | 376 ms: 1.11x slower                                                                                                    |
| pickle_pure_python         | 324 us                                                                                                            | 360 us: 1.11x slower                                                                                                    |
| mdp                        | 2.50 sec                                                                                                          | 2.79 sec: 1.11x slower                                                                                                  |
| xml_etree_generate         | 86.5 ms                                                                                                           | 96.6 ms: 1.12x slower                                                                                                   |
| logging_silent             | 99.6 ns                                                                                                           | 111 ns: 1.12x slower                                                                                                    |
| k_core                     | 2.06 sec                                                                                                          | 2.31 sec: 1.12x slower                                                                                                  |
| subparsers                 | 22.7 ms                                                                                                           | 25.6 ms: 1.13x slower                                                                                                   |
| many_optionals             | 1.04 ms                                                                                                           | 1.18 ms: 1.13x slower                                                                                                   |
| json_dumps                 | 11.2 ms                                                                                                           | 12.8 ms: 1.14x slower                                                                                                   |
| unpickle_pure_python       | 224 us                                                                                                            | 257 us: 1.14x slower                                                                                                    |
| pprint_safe_repr           | 737 ms                                                                                                            | 848 ms: 1.15x slower                                                                                                    |
| django_template            | 37.2 ms                                                                                                           | 43.1 ms: 1.16x slower                                                                                                   |
| 2to3                       | 258 ms                                                                                                            | 299 ms: 1.16x slower                                                                                                    |
| pprint_pformat             | 1.50 sec                                                                                                          | 1.74 sec: 1.16x slower                                                                                                  |
| sqlglot_normalize          | 104 ms                                                                                                            | 121 ms: 1.16x slower                                                                                                    |
| sqlglot_optimize           | 52.7 ms                                                                                                           | 61.4 ms: 1.16x slower                                                                                                   |
| genshi_xml                 | 51.0 ms                                                                                                           | 59.6 ms: 1.17x slower                                                                                                   |
| scimark_sor                | 116 ms                                                                                                            | 136 ms: 1.17x slower                                                                                                    |
| xml_etree_process          | 60.1 ms                                                                                                           | 70.4 ms: 1.17x slower                                                                                                   |
| thrift                     | 754 us                                                                                                            | 889 us: 1.18x slower                                                                                                    |
| scimark_fft                | 334 ms                                                                                                            | 395 ms: 1.18x slower                                                                                                    |
| telco                      | 7.64 ms                                                                                                           | 9.05 ms: 1.18x slower                                                                                                   |
| sympy_expand               | 465 ms                                                                                                            | 551 ms: 1.19x slower                                                                                                    |
| tomli_loads                | 2.00 sec                                                                                                          | 2.38 sec: 1.19x slower                                                                                                  |
| logging_simple             | 6.05 us                                                                                                           | 7.21 us: 1.19x slower                                                                                                   |
| sqlglot_transpile          | 1.62 ms                                                                                                           | 1.93 ms: 1.19x slower                                                                                                   |
| spectral_norm              | 95.9 ms                                                                                                           | 115 ms: 1.19x slower                                                                                                    |
| deepcopy_reduce            | 2.73 us                                                                                                           | 3.26 us: 1.19x slower                                                                                                   |
| deepcopy                   | 261 us                                                                                                            | 312 us: 1.20x slower                                                                                                    |
| sqlalchemy_imperative      | 19.8 ms                                                                                                           | 23.7 ms: 1.20x slower                                                                                                   |
| pyflate                    | 425 ms                                                                                                            | 509 ms: 1.20x slower                                                                                                    |
| chaos                      | 58.5 ms                                                                                                           | 70.1 ms: 1.20x slower                                                                                                   |
| sqlalchemy_declarative     | 131 ms                                                                                                            | 157 ms: 1.20x slower                                                                                                    |
| nqueens                    | 81.4 ms                                                                                                           | 97.8 ms: 1.20x slower                                                                                                   |
| sympy_str                  | 278 ms                                                                                                            | 335 ms: 1.20x slower                                                                                                    |
| sympy_sum                  | 156 ms                                                                                                            | 188 ms: 1.20x slower                                                                                                    |
| sympy_integrate            | 20.1 ms                                                                                                           | 24.2 ms: 1.21x slower                                                                                                   |
| raytrace                   | 267 ms                                                                                                            | 323 ms: 1.21x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.70 ms                                                                                                           | 5.68 ms: 1.21x slower                                                                                                   |
| scimark_lu                 | 114 ms                                                                                                            | 139 ms: 1.22x slower                                                                                                    |
| regex_compile              | 130 ms                                                                                                            | 158 ms: 1.22x slower                                                                                                    |
| sqlglot_parse              | 1.32 ms                                                                                                           | 1.61 ms: 1.22x slower                                                                                                   |
| logging_format             | 6.73 us                                                                                                           | 8.26 us: 1.23x slower                                                                                                   |
| comprehensions             | 17.2 us                                                                                                           | 21.1 us: 1.23x slower                                                                                                   |
| crypto_pyaes               | 71.5 ms                                                                                                           | 87.8 ms: 1.23x slower                                                                                                   |
| coverage                   | 81.1 ms                                                                                                           | 99.6 ms: 1.23x slower                                                                                                   |
| shortest_path              | 445 ms                                                                                                            | 548 ms: 1.23x slower                                                                                                    |
| fannkuch                   | 401 ms                                                                                                            | 499 ms: 1.24x slower                                                                                                    |
| typing_runtime_protocols   | 158 us                                                                                                            | 197 us: 1.25x slower                                                                                                    |
| deltablue                  | 3.12 ms                                                                                                           | 3.90 ms: 1.25x slower                                                                                                   |
| connected_components       | 402 ms                                                                                                            | 504 ms: 1.25x slower                                                                                                    |
| hexiom                     | 6.10 ms                                                                                                           | 7.65 ms: 1.25x slower                                                                                                   |
| deepcopy_memo              | 30.8 us                                                                                                           | 38.8 us: 1.26x slower                                                                                                   |
| scimark_monte_carlo        | 66.6 ms                                                                                                           | 84.1 ms: 1.26x slower                                                                                                   |
| go                         | 113 ms                                                                                                            | 145 ms: 1.28x slower                                                                                                    |
| richards_super             | 49.8 ms                                                                                                           | 63.7 ms: 1.28x slower                                                                                                   |
| genshi_text                | 21.9 ms                                                                                                           | 28.1 ms: 1.28x slower                                                                                                   |
| richards                   | 42.7 ms                                                                                                           | 55.1 ms: 1.29x slower                                                                                                   |
| meteor_contest             | 101 ms                                                                                                            | 131 ms: 1.29x slower                                                                                                    |
| python_startup_no_site     | 8.63 ms                                                                                                           | 11.2 ms: 1.29x slower                                                                                                   |
| nbody                      | 102 ms                                                                                                            | 134 ms: 1.31x slower                                                                                                    |
| mako                       | 12.1 ms                                                                                                           | 15.9 ms: 1.32x slower                                                                                                   |
| bench_thread_pool          | 1.05 ms                                                                                                           | 3.16 ms: 2.99x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json: html5lib

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.20x