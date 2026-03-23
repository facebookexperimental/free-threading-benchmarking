# Results vs. base

- fork: python
- ref: fb8d8d9c9f9cbc94fa58
- machine: linux-x86_64
- commit hash: fb8d8d9
- commit date: 2026-03-22
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                            | 283 ms: 1.14x slower                                                                                                    |
| docutils       | 2.52 sec                                                                                                          | 2.64 sec: 1.05x slower                                                                                                  |
| html5lib       | 60.3 ms                                                                                                           | 65.3 ms: 1.08x slower                                                                                                   |
| sphinx         | 965 ms                                                                                                            | 1.05 sec: 1.09x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets        | 544 ms                                                                                                            | 515 ms: 1.06x faster                                                                                                    |
| coroutines                | 23.8 ms                                                                                                           | 24.6 ms: 1.03x slower                                                                                                   |
| async_tree_memoization_tg | 302 ms                                                                                                            | 322 ms: 1.07x slower                                                                                                    |
| async_tree_io_tg          | 566 ms                                                                                                            | 607 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 528 ms                                                                                                            | 569 ms: 1.08x slower                                                                                                    |
| async_tree_none_tg        | 243 ms                                                                                                            | 262 ms: 1.08x slower                                                                                                    |
| async_tree_io             | 585 ms                                                                                                            | 645 ms: 1.10x slower                                                                                                    |
| async_generators          | 344 ms                                                                                                            | 380 ms: 1.10x slower                                                                                                    |
| async_tree_memoization    | 312 ms                                                                                                            | 351 ms: 1.12x slower                                                                                                    |
| async_tree_none           | 247 ms                                                                                                            | 288 ms: 1.17x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 70.1 ms                                                                                                           | 74.8 ms: 1.07x slower                                                                                                   |
| nbody          | 93.2 ms                                                                                                           | 127 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.9 ms                                                                                                           | 21.8 ms: 1.05x faster                                                                                                   |
| regex_effbot   | 2.96 ms                                                                                                           | 2.85 ms: 1.04x faster                                                                                                   |
| regex_dna      | 187 ms                                                                                                            | 181 ms: 1.03x faster                                                                                                    |
| regex_compile  | 124 ms                                                                                                            | 141 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 85.0 ms                                                                                                           | 87.7 ms: 1.03x slower                                                                                                   |
| pickle_pure_python   | 310 us                                                                                                            | 335 us: 1.08x slower                                                                                                    |
| json_dumps           | 10.2 ms                                                                                                           | 11.0 ms: 1.08x slower                                                                                                   |
| tomli_loads          | 1.79 sec                                                                                                          | 1.95 sec: 1.09x slower                                                                                                  |
| json_loads           | 27.9 us                                                                                                           | 30.7 us: 1.10x slower                                                                                                   |
| unpickle_pure_python | 214 us                                                                                                            | 237 us: 1.11x slower                                                                                                    |
| xml_etree_generate   | 84.6 ms                                                                                                           | 96.1 ms: 1.14x slower                                                                                                   |
| xml_etree_process    | 59.2 ms                                                                                                           | 68.4 ms: 1.16x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                                                           | 16.0 ms: 1.26x slower                                                                                                   |
| python_startup_no_site | 7.43 ms                                                                                                           | 9.77 ms: 1.31x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                                                                           | 54.0 ms: 1.08x slower                                                                                                   |
| django_template | 35.3 ms                                                                                                           | 39.7 ms: 1.13x slower                                                                                                   |
| genshi_text     | 21.3 ms                                                                                                           | 25.6 ms: 1.20x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 15.7 ms: 1.30x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.17x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json | results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool             | 262 ms                                                                                                            | 7.01 ms: 37.32x faster                                                                                                  |
| gc_traversal              | 4.28 ms                                                                                                           | 1.93 ms: 2.23x faster                                                                                                   |
| create_gc_cycles          | 1.86 ms                                                                                                           | 1.51 ms: 1.23x faster                                                                                                   |
| sqlite_synth              | 2.23 us                                                                                                           | 1.91 us: 1.17x faster                                                                                                   |
| asyncio_websockets        | 544 ms                                                                                                            | 515 ms: 1.06x faster                                                                                                    |
| regex_v8                  | 22.9 ms                                                                                                           | 21.8 ms: 1.05x faster                                                                                                   |
| regex_effbot              | 2.96 ms                                                                                                           | 2.85 ms: 1.04x faster                                                                                                   |
| regex_dna                 | 187 ms                                                                                                            | 181 ms: 1.03x faster                                                                                                    |
| pathlib                   | 17.5 ms                                                                                                           | 17.6 ms: 1.01x slower                                                                                                   |
| dulwich_log               | 69.2 ms                                                                                                           | 70.6 ms: 1.02x slower                                                                                                   |
| xml_etree_iterparse       | 85.0 ms                                                                                                           | 87.7 ms: 1.03x slower                                                                                                   |
| coroutines                | 23.8 ms                                                                                                           | 24.6 ms: 1.03x slower                                                                                                   |
| pycparser                 | 1.08 sec                                                                                                          | 1.12 sec: 1.04x slower                                                                                                  |
| logging_silent            | 99.9 ns                                                                                                           | 104 ns: 1.04x slower                                                                                                    |
| docutils                  | 2.52 sec                                                                                                          | 2.64 sec: 1.05x slower                                                                                                  |
| pylint                    | 282 ms                                                                                                            | 296 ms: 1.05x slower                                                                                                    |
| json                      | 5.08 ms                                                                                                           | 5.35 ms: 1.05x slower                                                                                                   |
| bpe_tokeniser             | 4.16 sec                                                                                                          | 4.41 sec: 1.06x slower                                                                                                  |
| async_tree_memoization_tg | 302 ms                                                                                                            | 322 ms: 1.07x slower                                                                                                    |
| float                     | 70.1 ms                                                                                                           | 74.8 ms: 1.07x slower                                                                                                   |
| deltablue                 | 3.26 ms                                                                                                           | 3.50 ms: 1.07x slower                                                                                                   |
| async_tree_io_tg          | 566 ms                                                                                                            | 607 ms: 1.07x slower                                                                                                    |
| genshi_xml                | 50.2 ms                                                                                                           | 54.0 ms: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed   | 528 ms                                                                                                            | 569 ms: 1.08x slower                                                                                                    |
| async_tree_none_tg        | 243 ms                                                                                                            | 262 ms: 1.08x slower                                                                                                    |
| sympy_expand              | 482 ms                                                                                                            | 520 ms: 1.08x slower                                                                                                    |
| many_optionals            | 943 us                                                                                                            | 1.02 ms: 1.08x slower                                                                                                   |
| pickle_pure_python        | 310 us                                                                                                            | 335 us: 1.08x slower                                                                                                    |
| json_dumps                | 10.2 ms                                                                                                           | 11.0 ms: 1.08x slower                                                                                                   |
| html5lib                  | 60.3 ms                                                                                                           | 65.3 ms: 1.08x slower                                                                                                   |
| sphinx                    | 965 ms                                                                                                            | 1.05 sec: 1.09x slower                                                                                                  |
| tomli_loads               | 1.79 sec                                                                                                          | 1.95 sec: 1.09x slower                                                                                                  |
| telco                     | 159 ms                                                                                                            | 173 ms: 1.09x slower                                                                                                    |
| pprint_safe_repr          | 722 ms                                                                                                            | 790 ms: 1.09x slower                                                                                                    |
| comprehensions            | 16.5 us                                                                                                           | 18.1 us: 1.10x slower                                                                                                   |
| json_loads                | 27.9 us                                                                                                           | 30.7 us: 1.10x slower                                                                                                   |
| subparsers                | 9.25 ms                                                                                                           | 10.2 ms: 1.10x slower                                                                                                   |
| async_tree_io             | 585 ms                                                                                                            | 645 ms: 1.10x slower                                                                                                    |
| async_generators          | 344 ms                                                                                                            | 380 ms: 1.10x slower                                                                                                    |
| unpickle_pure_python      | 214 us                                                                                                            | 237 us: 1.11x slower                                                                                                    |
| sympy_str                 | 278 ms                                                                                                            | 309 ms: 1.11x slower                                                                                                    |
| sympy_sum                 | 158 ms                                                                                                            | 176 ms: 1.12x slower                                                                                                    |
| scimark_sor               | 109 ms                                                                                                            | 122 ms: 1.12x slower                                                                                                    |
| pprint_pformat            | 1.47 sec                                                                                                          | 1.64 sec: 1.12x slower                                                                                                  |
| sqlglot_v2_normalize      | 103 ms                                                                                                            | 115 ms: 1.12x slower                                                                                                    |
| async_tree_memoization    | 312 ms                                                                                                            | 351 ms: 1.12x slower                                                                                                    |
| django_template           | 35.3 ms                                                                                                           | 39.7 ms: 1.13x slower                                                                                                   |
| sympy_integrate           | 19.2 ms                                                                                                           | 21.6 ms: 1.13x slower                                                                                                   |
| hexiom                    | 5.74 ms                                                                                                           | 6.48 ms: 1.13x slower                                                                                                   |
| sqlglot_v2_optimize       | 51.1 ms                                                                                                           | 57.8 ms: 1.13x slower                                                                                                   |
| deepcopy_reduce           | 2.60 us                                                                                                           | 2.94 us: 1.13x slower                                                                                                   |
| deepcopy                  | 235 us                                                                                                            | 266 us: 1.13x slower                                                                                                    |
| xml_etree_generate        | 84.6 ms                                                                                                           | 96.1 ms: 1.14x slower                                                                                                   |
| 2to3                      | 249 ms                                                                                                            | 283 ms: 1.14x slower                                                                                                    |
| mdp                       | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| pyflate                   | 402 ms                                                                                                            | 459 ms: 1.14x slower                                                                                                    |
| scimark_lu                | 110 ms                                                                                                            | 125 ms: 1.14x slower                                                                                                    |
| regex_compile             | 124 ms                                                                                                            | 141 ms: 1.14x slower                                                                                                    |
| nqueens                   | 77.0 ms                                                                                                           | 88.0 ms: 1.14x slower                                                                                                   |
| scimark_fft               | 308 ms                                                                                                            | 355 ms: 1.15x slower                                                                                                    |
| xml_etree_process         | 59.2 ms                                                                                                           | 68.4 ms: 1.16x slower                                                                                                   |
| go                        | 104 ms                                                                                                            | 121 ms: 1.16x slower                                                                                                    |
| chaos                     | 54.0 ms                                                                                                           | 62.5 ms: 1.16x slower                                                                                                   |
| sqlglot_v2_transpile      | 1.52 ms                                                                                                           | 1.77 ms: 1.16x slower                                                                                                   |
| async_tree_none           | 247 ms                                                                                                            | 288 ms: 1.17x slower                                                                                                    |
| generators                | 27.8 ms                                                                                                           | 32.5 ms: 1.17x slower                                                                                                   |
| thrift                    | 774 us                                                                                                            | 908 us: 1.17x slower                                                                                                    |
| deepcopy_memo             | 26.3 us                                                                                                           | 30.9 us: 1.17x slower                                                                                                   |
| logging_simple            | 5.80 us                                                                                                           | 6.81 us: 1.17x slower                                                                                                   |
| logging_format            | 6.62 us                                                                                                           | 7.81 us: 1.18x slower                                                                                                   |
| sqlglot_v2_parse          | 1.21 ms                                                                                                           | 1.43 ms: 1.18x slower                                                                                                   |
| k_core                    | 1.88 sec                                                                                                          | 2.24 sec: 1.19x slower                                                                                                  |
| raytrace                  | 251 ms                                                                                                            | 302 ms: 1.20x slower                                                                                                    |
| genshi_text               | 21.3 ms                                                                                                           | 25.6 ms: 1.20x slower                                                                                                   |
| fannkuch                  | 383 ms                                                                                                            | 460 ms: 1.20x slower                                                                                                    |
| meteor_contest            | 101 ms                                                                                                            | 123 ms: 1.21x slower                                                                                                    |
| bench_thread_pool         | 1.32 ms                                                                                                           | 1.62 ms: 1.22x slower                                                                                                   |
| typing_runtime_protocols  | 160 us                                                                                                            | 196 us: 1.22x slower                                                                                                    |
| shortest_path             | 432 ms                                                                                                            | 533 ms: 1.23x slower                                                                                                    |
| scimark_sparse_mat_mult   | 4.39 ms                                                                                                           | 5.47 ms: 1.25x slower                                                                                                   |
| richards_super            | 48.1 ms                                                                                                           | 60.0 ms: 1.25x slower                                                                                                   |
| connected_components      | 388 ms                                                                                                            | 486 ms: 1.25x slower                                                                                                    |
| richards                  | 42.2 ms                                                                                                           | 53.0 ms: 1.26x slower                                                                                                   |
| crypto_pyaes              | 69.5 ms                                                                                                           | 87.6 ms: 1.26x slower                                                                                                   |
| python_startup            | 12.7 ms                                                                                                           | 16.0 ms: 1.26x slower                                                                                                   |
| scimark_monte_carlo       | 62.4 ms                                                                                                           | 79.1 ms: 1.27x slower                                                                                                   |
| spectral_norm             | 90.3 ms                                                                                                           | 115 ms: 1.28x slower                                                                                                    |
| mako                      | 12.1 ms                                                                                                           | 15.7 ms: 1.30x slower                                                                                                   |
| python_startup_no_site    | 7.43 ms                                                                                                           | 9.77 ms: 1.31x slower                                                                                                   |
| coverage                  | 82.6 ms                                                                                                           | 112 ms: 1.36x slower                                                                                                    |
| nbody                     | 93.2 ms                                                                                                           | 127 ms: 1.36x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (3): xml_etree_parse, async_tree_cpu_io_mixed_tg, pidigits

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.21x