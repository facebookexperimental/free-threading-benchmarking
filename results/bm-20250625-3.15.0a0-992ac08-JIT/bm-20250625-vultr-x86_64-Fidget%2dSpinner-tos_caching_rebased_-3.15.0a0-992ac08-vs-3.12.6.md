# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tos_caching_rebased_
- machine: linux-x86_64
- commit hash: 992ac08
- commit date: 2025-06-25
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                            |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                                          |
| html5lib       | 63.6 ms                                                | 62.0 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.81x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                            |
| async_tree_io_tg           | 1.11 sec                                               | 633 ms: 1.75x faster                                                            |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                            |
| async_generators           | 384 ms                                                 | 356 ms: 1.08x faster                                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                                    |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.1 ms: 1.26x faster                                                           |
| nbody          | 89.3 ms                                                | 74.2 ms: 1.20x faster                                                           |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                            |
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                           |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                            |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.78 sec: 1.18x faster                                                          |
| unpickle_pure_python | 221 us                                                 | 195 us: 1.13x faster                                                            |
| xml_etree_generate   | 85.2 ms                                                | 78.1 ms: 1.09x faster                                                           |
| xml_etree_process    | 59.0 ms                                                | 54.6 ms: 1.08x faster                                                           |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                            |
| xml_etree_iterparse  | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                           |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                           |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.03x slower                                                           |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                           |
| mako           | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.81x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                            |
| async_tree_io_tg           | 1.11 sec                                               | 633 ms: 1.75x faster                                                            |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                            |
| richards                   | 45.9 ms                                                | 30.8 ms: 1.49x faster                                                           |
| richards_super             | 51.9 ms                                                | 35.0 ms: 1.48x faster                                                           |
| deepcopy_memo              | 40.3 us                                                | 28.4 us: 1.42x faster                                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                                            |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                            |
| spectral_norm              | 110 ms                                                 | 85.7 ms: 1.29x faster                                                           |
| float                      | 80.8 ms                                                | 64.1 ms: 1.26x faster                                                           |
| scimark_fft                | 342 ms                                                 | 280 ms: 1.22x faster                                                            |
| deltablue                  | 3.45 ms                                                | 2.85 ms: 1.21x faster                                                           |
| nbody                      | 89.3 ms                                                | 74.2 ms: 1.20x faster                                                           |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                            |
| go                         | 139 ms                                                 | 117 ms: 1.20x faster                                                            |
| bpe_tokeniser              | 4.74 sec                                               | 3.97 sec: 1.19x faster                                                          |
| tomli_loads                | 2.11 sec                                               | 1.78 sec: 1.18x faster                                                          |
| dulwich_log                | 78.9 ms                                                | 67.3 ms: 1.17x faster                                                           |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                                           |
| pyflate                    | 448 ms                                                 | 384 ms: 1.17x faster                                                            |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.16x faster                                                           |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 59.8 ms: 1.15x faster                                                           |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                                           |
| unpickle_pure_python       | 221 us                                                 | 195 us: 1.13x faster                                                            |
| pylint                     | 319 ms                                                 | 283 ms: 1.13x faster                                                            |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                           |
| chaos                      | 62.8 ms                                                | 56.6 ms: 1.11x faster                                                           |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                           |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                           |
| crypto_pyaes               | 76.6 ms                                                | 69.6 ms: 1.10x faster                                                           |
| xml_etree_generate         | 85.2 ms                                                | 78.1 ms: 1.09x faster                                                           |
| xml_etree_process          | 59.0 ms                                                | 54.6 ms: 1.08x faster                                                           |
| async_generators           | 384 ms                                                 | 356 ms: 1.08x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                            |
| thrift                     | 791 us                                                 | 737 us: 1.07x faster                                                            |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                           |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                            |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                                           |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                            |
| fannkuch                   | 372 ms                                                 | 355 ms: 1.05x faster                                                            |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                            |
| xml_etree_iterparse        | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                           |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                           |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                            |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                            |
| html5lib                   | 63.6 ms                                                | 62.0 ms: 1.03x faster                                                           |
| docutils                   | 2.64 sec                                               | 2.59 sec: 1.02x faster                                                          |
| logging_simple             | 6.63 us                                                | 6.53 us: 1.02x faster                                                           |
| logging_format             | 7.35 us                                                | 7.26 us: 1.01x faster                                                           |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                          |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.01x slower                                                            |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                           |
| sympy_expand               | 468 ms                                                 | 474 ms: 1.01x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                           |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.03x slower                                                           |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                           |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                           |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                            |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.73 ms: 1.08x slower                                                           |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                           |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                           |
| coverage                   | 71.4 ms                                                | 80.4 ms: 1.13x slower                                                           |
| telco                      | 6.53 ms                                                | 7.40 ms: 1.13x slower                                                           |
| pprint_safe_repr           | 743 ms                                                 | 857 ms: 1.15x slower                                                            |
| pprint_pformat             | 1.52 sec                                               | 1.78 sec: 1.17x slower                                                          |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                           |
| gc_traversal               | 3.46 ms                                                | 4.87 ms: 1.41x slower                                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.91 ms: 1.75x slower                                                           |
| logging_silent             | 109 ns                                                 | 471 ns: 4.32x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 99.1 ms: 9.18x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (5): sqlite_synth, genshi_xml, django_template, asyncio_websockets, hexiom
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased_-3.15.0a0-992ac08.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x