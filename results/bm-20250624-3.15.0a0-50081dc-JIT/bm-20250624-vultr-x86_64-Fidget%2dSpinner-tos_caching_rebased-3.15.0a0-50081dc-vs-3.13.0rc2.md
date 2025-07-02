# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tos_caching_rebased
- machine: linux-x86_64
- commit hash: 50081dc
- commit date: 2025-06-24
- overall geometric mean: 1.082x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.02x faster                                                           |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.02x faster                                                         |
| html5lib       | 67.0 ms                                                      | 61.6 ms: 1.09x faster                                                          |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.48x faster                                                           |
| async_tree_io_tg           | 913 ms                                                       | 627 ms: 1.46x faster                                                           |
| async_tree_io              | 876 ms                                                       | 613 ms: 1.43x faster                                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.33x faster                                                           |
| async_tree_none            | 354 ms                                                       | 271 ms: 1.30x faster                                                           |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                           |
| async_generators           | 377 ms                                                       | 351 ms: 1.08x faster                                                           |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                          |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                           |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 64.5 ms: 1.20x faster                                                          |
| nbody          | 85.1 ms                                                      | 76.1 ms: 1.12x faster                                                          |
| pidigits       | 217 ms                                                       | 209 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                        | 1.12x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.62 ms: 1.17x faster                                                          |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.08x faster                                                          |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                           |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                           |
| Geometric mean | (ref)                                                        | 1.09x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.77 sec: 1.13x faster                                                         |
| xml_etree_process    | 59.3 ms                                                      | 54.7 ms: 1.09x faster                                                          |
| unpickle_pure_python | 210 us                                                       | 194 us: 1.08x faster                                                           |
| xml_etree_generate   | 85.4 ms                                                      | 79.3 ms: 1.08x faster                                                          |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                           |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.9 ms: 1.03x faster                                                          |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.01x slower                                                          |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                          |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                                           |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                          |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                          |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                          |
| django_template | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                          |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                                   |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.04x faster                                                         |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.48x faster                                                           |
| richards                   | 45.2 ms                                                      | 31.0 ms: 1.46x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 627 ms: 1.46x faster                                                           |
| richards_super             | 51.6 ms                                                      | 35.6 ms: 1.45x faster                                                          |
| async_tree_io              | 876 ms                                                       | 613 ms: 1.43x faster                                                           |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                           |
| deepcopy_memo              | 39.1 us                                                      | 28.5 us: 1.37x faster                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.33x faster                                                           |
| async_tree_none            | 354 ms                                                       | 271 ms: 1.30x faster                                                           |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                           |
| spectral_norm              | 111 ms                                                       | 87.4 ms: 1.27x faster                                                          |
| scimark_fft                | 349 ms                                                       | 279 ms: 1.25x faster                                                           |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.24x faster                                                           |
| float                      | 77.5 ms                                                      | 64.5 ms: 1.20x faster                                                          |
| go                         | 141 ms                                                       | 118 ms: 1.19x faster                                                           |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                          |
| regex_effbot               | 3.08 ms                                                      | 2.62 ms: 1.17x faster                                                          |
| pyflate                    | 449 ms                                                       | 386 ms: 1.16x faster                                                           |
| tomli_loads                | 2.01 sec                                                     | 1.77 sec: 1.13x faster                                                         |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                                           |
| nbody                      | 85.1 ms                                                      | 76.1 ms: 1.12x faster                                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 3.98 sec: 1.12x faster                                                         |
| telco                      | 7.82 ms                                                      | 7.06 ms: 1.11x faster                                                          |
| dulwich_log                | 74.8 ms                                                      | 67.7 ms: 1.11x faster                                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 59.7 ms: 1.09x faster                                                          |
| html5lib                   | 67.0 ms                                                      | 61.6 ms: 1.09x faster                                                          |
| xml_etree_process          | 59.3 ms                                                      | 54.7 ms: 1.09x faster                                                          |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.08x faster                                                          |
| unpickle_pure_python       | 210 us                                                       | 194 us: 1.08x faster                                                           |
| deltablue                  | 3.12 ms                                                      | 2.90 ms: 1.08x faster                                                          |
| xml_etree_generate         | 85.4 ms                                                      | 79.3 ms: 1.08x faster                                                          |
| async_generators           | 377 ms                                                       | 351 ms: 1.08x faster                                                           |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                           |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                           |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                           |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.51 ms: 1.04x faster                                                          |
| nqueens                    | 78.6 ms                                                      | 75.5 ms: 1.04x faster                                                          |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                           |
| pidigits                   | 217 ms                                                       | 209 ms: 1.03x faster                                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.9 ms: 1.03x faster                                                          |
| generators                 | 28.8 ms                                                      | 27.9 ms: 1.03x faster                                                          |
| thrift                     | 778 us                                                       | 756 us: 1.03x faster                                                           |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                          |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                          |
| fannkuch                   | 370 ms                                                       | 362 ms: 1.02x faster                                                           |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                          |
| 2to3                       | 260 ms                                                       | 256 ms: 1.02x faster                                                           |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.02x faster                                                         |
| chaos                      | 57.3 ms                                                      | 56.5 ms: 1.01x faster                                                          |
| python_startup_no_site     | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                          |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                           |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                          |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                           |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                          |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.01x slower                                                          |
| json                       | 4.93 ms                                                      | 5.01 ms: 1.02x slower                                                          |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                         |
| django_template            | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                          |
| crypto_pyaes               | 67.9 ms                                                      | 69.4 ms: 1.02x slower                                                          |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                           |
| comprehensions             | 16.5 us                                                      | 16.9 us: 1.02x slower                                                          |
| sympy_expand               | 457 ms                                                       | 471 ms: 1.03x slower                                                           |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                          |
| hexiom                     | 5.99 ms                                                      | 6.29 ms: 1.05x slower                                                          |
| logging_simple             | 6.16 us                                                      | 6.47 us: 1.05x slower                                                          |
| logging_format             | 6.84 us                                                      | 7.23 us: 1.06x slower                                                          |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                                           |
| pprint_safe_repr           | 738 ms                                                       | 843 ms: 1.14x slower                                                           |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                          |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.75 sec: 1.17x slower                                                         |
| create_gc_cycles           | 1.34 ms                                                      | 1.89 ms: 1.41x slower                                                          |
| gc_traversal               | 3.14 ms                                                      | 4.65 ms: 1.48x slower                                                          |
| logging_silent             | 103 ns                                                       | 466 ns: 4.54x slower                                                           |
| bench_mp_pool              | 11.0 ms                                                      | 99.2 ms: 9.02x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                                   |

Benchmark hidden because not significant (5): genshi_xml, sympy_str, sqlite_synth, meteor_contest, sympy_sum
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x