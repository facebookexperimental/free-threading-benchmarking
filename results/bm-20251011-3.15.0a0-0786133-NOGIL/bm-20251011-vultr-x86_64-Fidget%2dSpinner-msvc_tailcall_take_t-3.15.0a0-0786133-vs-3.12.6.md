# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: msvc_tailcall_take_t
- machine: linux-x86_64
- commit hash: 0786133
- commit date: 2025-10-11
- overall geometric mean: 1.018x slower
- HPT reliability: 82.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                            |
| docutils       | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                          |
| html5lib       | 63.6 ms                                                | 67.5 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 514 ms: 2.16x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 541 ms: 2.00x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.98x faster                                                            |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                            |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                            |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                            |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                           |
| pidigits       | 184 ms                                                 | 204 ms: 1.11x slower                                                            |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                            |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                           |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                            |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                           |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                           |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                            |
| tomli_loads          | 2.11 sec                                               | 2.03 sec: 1.04x faster                                                          |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.07x slower                                                            |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                           |
| pickle_pure_python   | 308 us                                                 | 340 us: 1.11x slower                                                            |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                           |
| xml_etree_process    | 59.0 ms                                                | 69.7 ms: 1.18x slower                                                           |
| json_loads           | 26.5 us                                                | 31.7 us: 1.20x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                           |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                           |
| genshi_text     | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                           |
| django_template | 34.7 ms                                                | 41.8 ms: 1.21x slower                                                           |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 514 ms: 2.16x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 541 ms: 2.00x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.98x faster                                                            |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.84x faster                                                          |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                            |
| gc_traversal               | 3.46 ms                                                | 1.94 ms: 1.78x faster                                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                            |
| deepcopy_memo              | 40.3 us                                                | 31.1 us: 1.30x faster                                                           |
| deepcopy                   | 352 us                                                 | 279 us: 1.26x faster                                                            |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                           |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                           |
| float                      | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                           |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                            |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.11x faster                                                           |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                           |
| dulwich_log                | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                          |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                            |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                           |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                            |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                                           |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                            |
| tomli_loads                | 2.11 sec                                               | 2.03 sec: 1.04x faster                                                          |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                            |
| generators                 | 32.2 ms                                                | 31.1 ms: 1.04x faster                                                           |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                          |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                            |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                                            |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                            |
| scimark_fft                | 342 ms                                                 | 344 ms: 1.01x slower                                                            |
| chaos                      | 62.8 ms                                                | 63.5 ms: 1.01x slower                                                           |
| pyflate                    | 448 ms                                                 | 454 ms: 1.01x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                           |
| deltablue                  | 3.45 ms                                                | 3.53 ms: 1.03x slower                                                           |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                           |
| hexiom                     | 6.17 ms                                                | 6.36 ms: 1.03x slower                                                           |
| docutils                   | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                          |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                            |
| logging_simple             | 6.63 us                                                | 6.89 us: 1.04x slower                                                           |
| html5lib                   | 63.6 ms                                                | 67.5 ms: 1.06x slower                                                           |
| pprint_safe_repr           | 743 ms                                                 | 790 ms: 1.06x slower                                                            |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                            |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                            |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                            |
| logging_format             | 7.35 us                                                | 7.87 us: 1.07x slower                                                           |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                           |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.07x slower                                                            |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.08x slower                                                          |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                           |
| json                       | 5.02 ms                                                | 5.42 ms: 1.08x slower                                                           |
| nqueens                    | 80.1 ms                                                | 87.7 ms: 1.10x slower                                                           |
| pickle_pure_python         | 308 us                                                 | 340 us: 1.11x slower                                                            |
| richards                   | 45.9 ms                                                | 50.9 ms: 1.11x slower                                                           |
| pidigits                   | 184 ms                                                 | 204 ms: 1.11x slower                                                            |
| sympy_expand               | 468 ms                                                 | 519 ms: 1.11x slower                                                            |
| crypto_pyaes               | 76.6 ms                                                | 85.4 ms: 1.12x slower                                                           |
| thrift                     | 791 us                                                 | 884 us: 1.12x slower                                                            |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                           |
| richards_super             | 51.9 ms                                                | 59.1 ms: 1.14x slower                                                           |
| typing_runtime_protocols   | 163 us                                                 | 187 us: 1.15x slower                                                            |
| genshi_xml                 | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 79.1 ms: 1.16x slower                                                           |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.16x slower                                                            |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                            |
| genshi_text                | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                           |
| xml_etree_process          | 59.0 ms                                                | 69.7 ms: 1.18x slower                                                           |
| json_loads                 | 26.5 us                                                | 31.7 us: 1.20x slower                                                           |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.21x slower                                                           |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.32 ms: 1.21x slower                                                           |
| fannkuch                   | 372 ms                                                 | 452 ms: 1.21x slower                                                            |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.38x slower                                                           |
| bench_mp_pool              | 10.8 ms                                                | 15.2 ms: 1.41x slower                                                           |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                            |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                           |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                            |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                           |
| bench_thread_pool          | 941 us                                                 | 3.06 ms: 3.25x slower                                                           |
| telco                      | 6.53 ms                                                | 176 ms: 26.98x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                                    |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%2dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.018x slower

# HPT report

- Reliability score: 82.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x