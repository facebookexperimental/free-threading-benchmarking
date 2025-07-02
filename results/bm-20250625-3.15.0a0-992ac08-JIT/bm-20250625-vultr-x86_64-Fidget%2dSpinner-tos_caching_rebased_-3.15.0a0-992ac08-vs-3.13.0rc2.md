# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tos_caching_rebased_
- machine: linux-x86_64
- commit hash: 992ac08
- commit date: 2025-06-25
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                            |
| docutils       | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                                          |
| html5lib       | 67.0 ms                                                      | 62.0 ms: 1.08x faster                                                           |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                            |
| async_tree_io_tg           | 913 ms                                                       | 633 ms: 1.44x faster                                                            |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                            |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 511 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 511 ms: 1.25x faster                                                            |
| async_generators           | 377 ms                                                       | 356 ms: 1.06x faster                                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                           |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                            |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 64.1 ms: 1.21x faster                                                           |
| nbody          | 85.1 ms                                                      | 74.2 ms: 1.15x faster                                                           |
| pidigits       | 217 ms                                                       | 196 ms: 1.11x faster                                                            |
| Geometric mean | (ref)                                                        | 1.15x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                           |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                            |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                    |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.78 sec: 1.13x faster                                                          |
| xml_etree_generate   | 85.4 ms                                                      | 78.1 ms: 1.09x faster                                                           |
| xml_etree_process    | 59.3 ms                                                      | 54.6 ms: 1.09x faster                                                           |
| unpickle_pure_python | 210 us                                                       | 195 us: 1.08x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                            |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.3 ms: 1.03x faster                                                           |
| json_dumps           | 10.5 ms                                                      | 10.6 ms: 1.01x slower                                                           |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                           |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                           |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                           |
| mako            | 11.3 ms                                                      | 11.4 ms: 1.00x slower                                                           |
| django_template | 34.1 ms                                                      | 34.6 ms: 1.01x slower                                                           |
| genshi_xml      | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                           |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.03x faster                                                          |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                            |
| richards_super             | 51.6 ms                                                      | 35.0 ms: 1.48x faster                                                           |
| richards                   | 45.2 ms                                                      | 30.8 ms: 1.47x faster                                                           |
| async_tree_io_tg           | 913 ms                                                       | 633 ms: 1.44x faster                                                            |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                            |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                            |
| deepcopy_memo              | 39.1 us                                                      | 28.4 us: 1.38x faster                                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                            |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 511 ms: 1.30x faster                                                            |
| spectral_norm              | 111 ms                                                       | 85.7 ms: 1.30x faster                                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 511 ms: 1.25x faster                                                            |
| scimark_fft                | 349 ms                                                       | 280 ms: 1.25x faster                                                            |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                            |
| float                      | 77.5 ms                                                      | 64.1 ms: 1.21x faster                                                           |
| go                         | 141 ms                                                       | 117 ms: 1.21x faster                                                            |
| deepcopy_reduce            | 3.11 us                                                      | 2.64 us: 1.18x faster                                                           |
| pyflate                    | 449 ms                                                       | 384 ms: 1.17x faster                                                            |
| nbody                      | 85.1 ms                                                      | 74.2 ms: 1.15x faster                                                           |
| tomli_loads                | 2.01 sec                                                     | 1.78 sec: 1.13x faster                                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 3.97 sec: 1.12x faster                                                          |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                            |
| dulwich_log                | 74.8 ms                                                      | 67.3 ms: 1.11x faster                                                           |
| pidigits                   | 217 ms                                                       | 196 ms: 1.11x faster                                                            |
| deltablue                  | 3.12 ms                                                      | 2.85 ms: 1.10x faster                                                           |
| scimark_monte_carlo        | 65.4 ms                                                      | 59.8 ms: 1.09x faster                                                           |
| xml_etree_generate         | 85.4 ms                                                      | 78.1 ms: 1.09x faster                                                           |
| xml_etree_process          | 59.3 ms                                                      | 54.6 ms: 1.09x faster                                                           |
| html5lib                   | 67.0 ms                                                      | 62.0 ms: 1.08x faster                                                           |
| regex_effbot               | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                           |
| unpickle_pure_python       | 210 us                                                       | 195 us: 1.08x faster                                                            |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                            |
| async_generators           | 377 ms                                                       | 356 ms: 1.06x faster                                                            |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                            |
| telco                      | 7.82 ms                                                      | 7.40 ms: 1.06x faster                                                           |
| thrift                     | 778 us                                                       | 737 us: 1.06x faster                                                            |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                           |
| nqueens                    | 78.6 ms                                                      | 75.4 ms: 1.04x faster                                                           |
| fannkuch                   | 370 ms                                                       | 355 ms: 1.04x faster                                                            |
| coverage                   | 83.0 ms                                                      | 80.4 ms: 1.03x faster                                                           |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.3 ms: 1.03x faster                                                           |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                            |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                           |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                           |
| chaos                      | 57.3 ms                                                      | 56.6 ms: 1.01x faster                                                           |
| docutils                   | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                                          |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                           |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                            |
| python_startup_no_site     | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                           |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                            |
| mako                       | 11.3 ms                                                      | 11.4 ms: 1.00x slower                                                           |
| json_dumps                 | 10.5 ms                                                      | 10.6 ms: 1.01x slower                                                           |
| raytrace                   | 253 ms                                                       | 256 ms: 1.01x slower                                                            |
| django_template            | 34.1 ms                                                      | 34.6 ms: 1.01x slower                                                           |
| genshi_xml                 | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                           |
| crypto_pyaes               | 67.9 ms                                                      | 69.6 ms: 1.03x slower                                                           |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                           |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                           |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                           |
| hexiom                     | 5.99 ms                                                      | 6.19 ms: 1.03x slower                                                           |
| sympy_expand               | 457 ms                                                       | 474 ms: 1.04x slower                                                            |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.04x slower                                                          |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                            |
| logging_simple             | 6.16 us                                                      | 6.53 us: 1.06x slower                                                           |
| logging_format             | 6.84 us                                                      | 7.26 us: 1.06x slower                                                           |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                           |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                           |
| pprint_safe_repr           | 738 ms                                                       | 857 ms: 1.16x slower                                                            |
| pprint_pformat             | 1.50 sec                                                     | 1.78 sec: 1.19x slower                                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                           |
| gc_traversal               | 3.14 ms                                                      | 4.87 ms: 1.55x slower                                                           |
| logging_silent             | 103 ns                                                       | 471 ns: 4.59x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 99.1 ms: 9.02x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                                    |

Benchmark hidden because not significant (7): regex_dna, sympy_sum, regex_v8, pathlib, sympy_str, scimark_sparse_mat_mult, typing_runtime_protocols
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x