# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tos_caching_rebased
- machine: linux-x86_64
- commit hash: 50081dc
- commit date: 2025-06-24
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                           |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                         |
| html5lib       | 63.6 ms                                                | 61.6 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                           |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                           |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                           |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                           |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                           |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                           |
| async_generators           | 384 ms                                                 | 351 ms: 1.10x faster                                                           |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                                   |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.5 ms: 1.25x faster                                                          |
| nbody          | 89.3 ms                                                | 76.1 ms: 1.17x faster                                                          |
| pidigits       | 184 ms                                                 | 209 ms: 1.14x slower                                                           |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.62 ms: 1.21x faster                                                          |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                           |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                          |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                  | 1.07x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                         |
| unpickle_pure_python | 221 us                                                 | 194 us: 1.13x faster                                                           |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                           |
| xml_etree_process    | 59.0 ms                                                | 54.7 ms: 1.08x faster                                                          |
| xml_etree_generate   | 85.2 ms                                                | 79.3 ms: 1.07x faster                                                          |
| xml_etree_iterparse  | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                          |
| pickle_pure_python   | 308 us                                                 | 312 us: 1.01x slower                                                           |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                          |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                          |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                          |
| genshi_xml      | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                          |
| django_template | 34.7 ms                                                | 34.8 ms: 1.00x slower                                                          |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                           |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                           |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                           |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                           |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                           |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                           |
| richards                   | 45.9 ms                                                | 31.0 ms: 1.48x faster                                                          |
| richards_super             | 51.9 ms                                                | 35.6 ms: 1.46x faster                                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                           |
| deepcopy_memo              | 40.3 us                                                | 28.5 us: 1.41x faster                                                          |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                           |
| spectral_norm              | 110 ms                                                 | 87.4 ms: 1.26x faster                                                          |
| float                      | 80.8 ms                                                | 64.5 ms: 1.25x faster                                                          |
| scimark_fft                | 342 ms                                                 | 279 ms: 1.22x faster                                                           |
| regex_effbot               | 3.17 ms                                                | 2.62 ms: 1.21x faster                                                          |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                           |
| deltablue                  | 3.45 ms                                                | 2.90 ms: 1.19x faster                                                          |
| tomli_loads                | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                         |
| bpe_tokeniser              | 4.74 sec                                               | 3.98 sec: 1.19x faster                                                         |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                           |
| comprehensions             | 19.8 us                                                | 16.9 us: 1.18x faster                                                          |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.17x faster                                                          |
| nbody                      | 89.3 ms                                                | 76.1 ms: 1.17x faster                                                          |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                                           |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.17x faster                                                          |
| pyflate                    | 448 ms                                                 | 386 ms: 1.16x faster                                                           |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.16x faster                                                          |
| scimark_monte_carlo        | 68.4 ms                                                | 59.7 ms: 1.15x faster                                                          |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                           |
| unpickle_pure_python       | 221 us                                                 | 194 us: 1.13x faster                                                           |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                           |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                          |
| chaos                      | 62.8 ms                                                | 56.5 ms: 1.11x faster                                                          |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                          |
| crypto_pyaes               | 76.6 ms                                                | 69.4 ms: 1.10x faster                                                          |
| async_generators           | 384 ms                                                 | 351 ms: 1.10x faster                                                           |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                           |
| xml_etree_process          | 59.0 ms                                                | 54.7 ms: 1.08x faster                                                          |
| xml_etree_generate         | 85.2 ms                                                | 79.3 ms: 1.07x faster                                                          |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.07x faster                                                          |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                           |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                           |
| nqueens                    | 80.1 ms                                                | 75.5 ms: 1.06x faster                                                          |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.05x faster                                                           |
| xml_etree_iterparse        | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                          |
| thrift                     | 791 us                                                 | 756 us: 1.05x faster                                                           |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                          |
| html5lib                   | 63.6 ms                                                | 61.6 ms: 1.03x faster                                                          |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                          |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                           |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                           |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                         |
| fannkuch                   | 372 ms                                                 | 362 ms: 1.03x faster                                                           |
| logging_simple             | 6.63 us                                                | 6.47 us: 1.02x faster                                                          |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                         |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                           |
| logging_format             | 7.35 us                                                | 7.23 us: 1.02x faster                                                          |
| django_template            | 34.7 ms                                                | 34.8 ms: 1.00x slower                                                          |
| sympy_expand               | 468 ms                                                 | 471 ms: 1.01x slower                                                           |
| pickle_pure_python         | 308 us                                                 | 312 us: 1.01x slower                                                           |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                          |
| hexiom                     | 6.17 ms                                                | 6.29 ms: 1.02x slower                                                          |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                           |
| python_startup_no_site     | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.51 ms: 1.03x slower                                                          |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                          |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                          |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                          |
| telco                      | 6.53 ms                                                | 7.06 ms: 1.08x slower                                                          |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                          |
| pprint_safe_repr           | 743 ms                                                 | 843 ms: 1.13x slower                                                           |
| pidigits                   | 184 ms                                                 | 209 ms: 1.14x slower                                                           |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                                          |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                         |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                          |
| gc_traversal               | 3.46 ms                                                | 4.65 ms: 1.35x slower                                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.73x slower                                                          |
| logging_silent             | 109 ns                                                 | 466 ns: 4.27x slower                                                           |
| bench_mp_pool              | 10.8 ms                                                | 99.2 ms: 9.18x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                   |

Benchmark hidden because not significant (3): json, asyncio_websockets, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x