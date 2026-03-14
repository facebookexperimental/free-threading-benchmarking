# Results vs. base

- fork: python
- ref: 3c38feb2a21aacdb009e
- machine: linux-x86_64
- commit hash: 3c38feb
- commit date: 2026-03-13
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                                                            | 279 ms: 1.11x slower                                                                                                    |
| docutils       | 2.49 sec                                                                                                          | 2.62 sec: 1.05x slower                                                                                                  |
| html5lib       | 59.6 ms                                                                                                           | 65.4 ms: 1.10x slower                                                                                                   |
| sphinx         | 967 ms                                                                                                            | 1.04 sec: 1.08x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets        | 544 ms                                                                                                            | 513 ms: 1.06x faster                                                                                                    |
| coroutines                | 23.6 ms                                                                                                           | 23.8 ms: 1.01x slower                                                                                                   |
| async_tree_io_tg          | 567 ms                                                                                                            | 591 ms: 1.04x slower                                                                                                    |
| async_tree_memoization_tg | 304 ms                                                                                                            | 322 ms: 1.06x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 506 ms                                                                                                            | 537 ms: 1.06x slower                                                                                                    |
| async_tree_none_tg        | 243 ms                                                                                                            | 258 ms: 1.06x slower                                                                                                    |
| async_tree_io             | 585 ms                                                                                                            | 631 ms: 1.08x slower                                                                                                    |
| async_generators          | 341 ms                                                                                                            | 371 ms: 1.09x slower                                                                                                    |
| async_tree_memoization    | 309 ms                                                                                                            | 346 ms: 1.12x slower                                                                                                    |
| async_tree_none           | 248 ms                                                                                                            | 284 ms: 1.15x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 205 ms                                                                                                            | 188 ms: 1.09x faster                                                                                                    |
| float          | 69.5 ms                                                                                                           | 73.4 ms: 1.06x slower                                                                                                   |
| nbody          | 96.0 ms                                                                                                           | 121 ms: 1.26x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                           | 21.5 ms: 1.01x faster                                                                                                   |
| regex_dna      | 170 ms                                                                                                            | 176 ms: 1.03x slower                                                                                                    |
| regex_effbot   | 2.82 ms                                                                                                           | 2.92 ms: 1.04x slower                                                                                                   |
| regex_compile  | 124 ms                                                                                                            | 142 ms: 1.15x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 131 ms                                                                                                            | 132 ms: 1.01x slower                                                                                                    |
| xml_etree_iterparse  | 85.2 ms                                                                                                           | 89.0 ms: 1.04x slower                                                                                                   |
| tomli_loads          | 1.81 sec                                                                                                          | 1.94 sec: 1.07x slower                                                                                                  |
| pickle_pure_python   | 309 us                                                                                                            | 333 us: 1.08x slower                                                                                                    |
| json_loads           | 27.5 us                                                                                                           | 30.3 us: 1.10x slower                                                                                                   |
| json_dumps           | 9.82 ms                                                                                                           | 10.9 ms: 1.12x slower                                                                                                   |
| unpickle_pure_python | 210 us                                                                                                            | 238 us: 1.13x slower                                                                                                    |
| xml_etree_generate   | 83.6 ms                                                                                                           | 94.7 ms: 1.13x slower                                                                                                   |
| xml_etree_process    | 59.5 ms                                                                                                           | 67.8 ms: 1.14x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                           | 15.9 ms: 1.26x slower                                                                                                   |
| python_startup_no_site | 7.44 ms                                                                                                           | 9.75 ms: 1.31x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                                                           | 39.9 ms: 1.11x slower                                                                                                   |
| genshi_xml      | 48.8 ms                                                                                                           | 54.5 ms: 1.12x slower                                                                                                   |
| genshi_text     | 20.8 ms                                                                                                           | 26.1 ms: 1.25x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 15.6 ms: 1.29x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.19x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20260313-3.15.0a7+-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json | results/bm-20260313-3.15.0a7+-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7+-3c38feb.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool             | 275 ms                                                                                                            | 7.00 ms: 39.23x faster                                                                                                  |
| gc_traversal              | 4.65 ms                                                                                                           | 1.93 ms: 2.41x faster                                                                                                   |
| create_gc_cycles          | 1.86 ms                                                                                                           | 1.51 ms: 1.23x faster                                                                                                   |
| sqlite_synth              | 2.24 us                                                                                                           | 1.94 us: 1.15x faster                                                                                                   |
| pidigits                  | 205 ms                                                                                                            | 188 ms: 1.09x faster                                                                                                    |
| asyncio_websockets        | 544 ms                                                                                                            | 513 ms: 1.06x faster                                                                                                    |
| regex_v8                  | 21.7 ms                                                                                                           | 21.5 ms: 1.01x faster                                                                                                   |
| xml_etree_parse           | 131 ms                                                                                                            | 132 ms: 1.01x slower                                                                                                    |
| pycparser                 | 1.11 sec                                                                                                          | 1.12 sec: 1.01x slower                                                                                                  |
| coroutines                | 23.6 ms                                                                                                           | 23.8 ms: 1.01x slower                                                                                                   |
| pathlib                   | 17.2 ms                                                                                                           | 17.5 ms: 1.02x slower                                                                                                   |
| logging_silent            | 102 ns                                                                                                            | 104 ns: 1.02x slower                                                                                                    |
| regex_dna                 | 170 ms                                                                                                            | 176 ms: 1.03x slower                                                                                                    |
| dulwich_log               | 67.5 ms                                                                                                           | 69.8 ms: 1.03x slower                                                                                                   |
| regex_effbot              | 2.82 ms                                                                                                           | 2.92 ms: 1.04x slower                                                                                                   |
| async_tree_io_tg          | 567 ms                                                                                                            | 591 ms: 1.04x slower                                                                                                    |
| deltablue                 | 3.31 ms                                                                                                           | 3.45 ms: 1.04x slower                                                                                                   |
| xml_etree_iterparse       | 85.2 ms                                                                                                           | 89.0 ms: 1.04x slower                                                                                                   |
| pylint                    | 285 ms                                                                                                            | 299 ms: 1.05x slower                                                                                                    |
| bpe_tokeniser             | 4.15 sec                                                                                                          | 4.37 sec: 1.05x slower                                                                                                  |
| docutils                  | 2.49 sec                                                                                                          | 2.62 sec: 1.05x slower                                                                                                  |
| float                     | 69.5 ms                                                                                                           | 73.4 ms: 1.06x slower                                                                                                   |
| json                      | 5.04 ms                                                                                                           | 5.33 ms: 1.06x slower                                                                                                   |
| sympy_expand              | 485 ms                                                                                                            | 514 ms: 1.06x slower                                                                                                    |
| async_tree_memoization_tg | 304 ms                                                                                                            | 322 ms: 1.06x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 506 ms                                                                                                            | 537 ms: 1.06x slower                                                                                                    |
| many_optionals            | 942 us                                                                                                            | 1.00 ms: 1.06x slower                                                                                                   |
| async_tree_none_tg        | 243 ms                                                                                                            | 258 ms: 1.06x slower                                                                                                    |
| tomli_loads               | 1.81 sec                                                                                                          | 1.94 sec: 1.07x slower                                                                                                  |
| telco                     | 157 ms                                                                                                            | 169 ms: 1.08x slower                                                                                                    |
| pickle_pure_python        | 309 us                                                                                                            | 333 us: 1.08x slower                                                                                                    |
| async_tree_io             | 585 ms                                                                                                            | 631 ms: 1.08x slower                                                                                                    |
| sphinx                    | 967 ms                                                                                                            | 1.04 sec: 1.08x slower                                                                                                  |
| async_generators          | 341 ms                                                                                                            | 371 ms: 1.09x slower                                                                                                    |
| html5lib                  | 59.6 ms                                                                                                           | 65.4 ms: 1.10x slower                                                                                                   |
| json_loads                | 27.5 us                                                                                                           | 30.3 us: 1.10x slower                                                                                                   |
| sympy_str                 | 279 ms                                                                                                            | 308 ms: 1.10x slower                                                                                                    |
| subparsers                | 9.11 ms                                                                                                           | 10.1 ms: 1.11x slower                                                                                                   |
| pprint_safe_repr          | 719 ms                                                                                                            | 797 ms: 1.11x slower                                                                                                    |
| django_template           | 35.8 ms                                                                                                           | 39.9 ms: 1.11x slower                                                                                                   |
| 2to3                      | 251 ms                                                                                                            | 279 ms: 1.11x slower                                                                                                    |
| json_dumps                | 9.82 ms                                                                                                           | 10.9 ms: 1.12x slower                                                                                                   |
| sympy_sum                 | 159 ms                                                                                                            | 178 ms: 1.12x slower                                                                                                    |
| genshi_xml                | 48.8 ms                                                                                                           | 54.5 ms: 1.12x slower                                                                                                   |
| async_tree_memoization    | 309 ms                                                                                                            | 346 ms: 1.12x slower                                                                                                    |
| sqlglot_v2_normalize      | 102 ms                                                                                                            | 114 ms: 1.12x slower                                                                                                    |
| scimark_lu                | 111 ms                                                                                                            | 125 ms: 1.12x slower                                                                                                    |
| pprint_pformat            | 1.47 sec                                                                                                          | 1.65 sec: 1.13x slower                                                                                                  |
| logging_simple            | 5.97 us                                                                                                           | 6.72 us: 1.13x slower                                                                                                   |
| sqlglot_v2_optimize       | 51.2 ms                                                                                                           | 57.7 ms: 1.13x slower                                                                                                   |
| scimark_fft               | 311 ms                                                                                                            | 351 ms: 1.13x slower                                                                                                    |
| unpickle_pure_python      | 210 us                                                                                                            | 238 us: 1.13x slower                                                                                                    |
| xml_etree_generate        | 83.6 ms                                                                                                           | 94.7 ms: 1.13x slower                                                                                                   |
| deepcopy_reduce           | 2.56 us                                                                                                           | 2.90 us: 1.13x slower                                                                                                   |
| comprehensions            | 16.0 us                                                                                                           | 18.2 us: 1.13x slower                                                                                                   |
| sympy_integrate           | 19.1 ms                                                                                                           | 21.6 ms: 1.13x slower                                                                                                   |
| go                        | 105 ms                                                                                                            | 119 ms: 1.14x slower                                                                                                    |
| scimark_sor               | 107 ms                                                                                                            | 121 ms: 1.14x slower                                                                                                    |
| xml_etree_process         | 59.5 ms                                                                                                           | 67.8 ms: 1.14x slower                                                                                                   |
| deepcopy                  | 233 us                                                                                                            | 266 us: 1.14x slower                                                                                                    |
| mdp                       | 1.15 sec                                                                                                          | 1.32 sec: 1.14x slower                                                                                                  |
| chaos                     | 54.1 ms                                                                                                           | 61.9 ms: 1.14x slower                                                                                                   |
| async_tree_none           | 248 ms                                                                                                            | 284 ms: 1.15x slower                                                                                                    |
| pyflate                   | 405 ms                                                                                                            | 465 ms: 1.15x slower                                                                                                    |
| regex_compile             | 124 ms                                                                                                            | 142 ms: 1.15x slower                                                                                                    |
| hexiom                    | 5.65 ms                                                                                                           | 6.54 ms: 1.16x slower                                                                                                   |
| logging_format            | 6.58 us                                                                                                           | 7.63 us: 1.16x slower                                                                                                   |
| sqlglot_v2_transpile      | 1.51 ms                                                                                                           | 1.75 ms: 1.16x slower                                                                                                   |
| thrift                    | 767 us                                                                                                            | 894 us: 1.17x slower                                                                                                    |
| scimark_sparse_mat_mult   | 4.45 ms                                                                                                           | 5.21 ms: 1.17x slower                                                                                                   |
| k_core                    | 1.88 sec                                                                                                          | 2.21 sec: 1.18x slower                                                                                                  |
| deepcopy_memo             | 26.4 us                                                                                                           | 31.2 us: 1.18x slower                                                                                                   |
| generators                | 27.6 ms                                                                                                           | 32.7 ms: 1.18x slower                                                                                                   |
| typing_runtime_protocols  | 160 us                                                                                                            | 190 us: 1.19x slower                                                                                                    |
| sqlglot_v2_parse          | 1.21 ms                                                                                                           | 1.43 ms: 1.19x slower                                                                                                   |
| fannkuch                  | 386 ms                                                                                                            | 461 ms: 1.19x slower                                                                                                    |
| raytrace                  | 252 ms                                                                                                            | 301 ms: 1.19x slower                                                                                                    |
| spectral_norm             | 92.3 ms                                                                                                           | 111 ms: 1.20x slower                                                                                                    |
| nqueens                   | 73.9 ms                                                                                                           | 89.0 ms: 1.20x slower                                                                                                   |
| richards                  | 42.4 ms                                                                                                           | 51.4 ms: 1.21x slower                                                                                                   |
| meteor_contest            | 101 ms                                                                                                            | 123 ms: 1.21x slower                                                                                                    |
| richards_super            | 48.3 ms                                                                                                           | 58.6 ms: 1.21x slower                                                                                                   |
| bench_thread_pool         | 1.33 ms                                                                                                           | 1.63 ms: 1.22x slower                                                                                                   |
| shortest_path             | 431 ms                                                                                                            | 535 ms: 1.24x slower                                                                                                    |
| connected_components      | 389 ms                                                                                                            | 485 ms: 1.25x slower                                                                                                    |
| genshi_text               | 20.8 ms                                                                                                           | 26.1 ms: 1.25x slower                                                                                                   |
| python_startup            | 12.6 ms                                                                                                           | 15.9 ms: 1.26x slower                                                                                                   |
| scimark_monte_carlo       | 62.2 ms                                                                                                           | 78.4 ms: 1.26x slower                                                                                                   |
| nbody                     | 96.0 ms                                                                                                           | 121 ms: 1.26x slower                                                                                                    |
| crypto_pyaes              | 68.9 ms                                                                                                           | 87.3 ms: 1.27x slower                                                                                                   |
| mako                      | 12.1 ms                                                                                                           | 15.6 ms: 1.29x slower                                                                                                   |
| python_startup_no_site    | 7.44 ms                                                                                                           | 9.75 ms: 1.31x slower                                                                                                   |
| coverage                  | 81.2 ms                                                                                                           | 114 ms: 1.40x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x