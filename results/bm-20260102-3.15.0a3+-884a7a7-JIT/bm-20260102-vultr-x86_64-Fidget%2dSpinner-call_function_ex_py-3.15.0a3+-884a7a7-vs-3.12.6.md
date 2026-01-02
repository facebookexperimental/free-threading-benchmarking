# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: call_function_ex_py
- machine: linux-x86_64
- commit hash: 884a7a7
- commit date: 2026-01-02
- overall geometric mean: 1.121x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                                            |
| docutils       | 2.64 sec                                               | 2.71 sec: 1.03x slower                                                          |
| html5lib       | 63.6 ms                                                | 64.6 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                            |
| async_tree_none            | 464 ms                                                 | 237 ms: 1.96x faster                                                            |
| async_tree_io_tg           | 1.11 sec                                               | 581 ms: 1.91x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.89x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 296 ms: 1.88x faster                                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                                            |
| async_generators           | 384 ms                                                 | 353 ms: 1.09x faster                                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                           |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 57.6 ms: 1.40x faster                                                           |
| nbody          | 89.3 ms                                                | 74.1 ms: 1.21x faster                                                           |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                  | 1.15x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 121 ms: 1.18x faster                                                            |
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                           |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                            |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 176 us: 1.25x faster                                                            |
| xml_etree_iterparse  | 96.7 ms                                                | 83.0 ms: 1.17x faster                                                           |
| pickle_pure_python   | 308 us                                                 | 276 us: 1.11x faster                                                            |
| xml_etree_process    | 59.0 ms                                                | 53.8 ms: 1.10x faster                                                           |
| xml_etree_generate   | 85.2 ms                                                | 78.4 ms: 1.09x faster                                                           |
| json_dumps           | 10.4 ms                                                | 9.55 ms: 1.08x faster                                                           |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                            |
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                          |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                           |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                           |
| mako           | 11.0 ms                                                | 10.4 ms: 1.05x faster                                                           |
| genshi_xml     | 50.2 ms                                                | 53.7 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 18.2 ms: 2.53x faster                                                           |
| richards_super             | 51.9 ms                                                | 21.5 ms: 2.42x faster                                                           |
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                            |
| async_tree_none            | 464 ms                                                 | 237 ms: 1.96x faster                                                            |
| async_tree_io_tg           | 1.11 sec                                               | 581 ms: 1.91x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.89x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 296 ms: 1.88x faster                                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                            |
| mdp                        | 2.42 sec                                               | 1.35 sec: 1.80x faster                                                          |
| deepcopy_memo              | 40.3 us                                                | 24.6 us: 1.64x faster                                                           |
| go                         | 139 ms                                                 | 91.5 ms: 1.52x faster                                                           |
| deepcopy                   | 352 us                                                 | 241 us: 1.46x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                                            |
| float                      | 80.8 ms                                                | 57.6 ms: 1.40x faster                                                           |
| scimark_fft                | 342 ms                                                 | 257 ms: 1.33x faster                                                            |
| logging_silent             | 109 ns                                                 | 82.6 ns: 1.32x faster                                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 52.0 ms: 1.31x faster                                                           |
| deltablue                  | 3.45 ms                                                | 2.66 ms: 1.30x faster                                                           |
| scimark_sor                | 130 ms                                                 | 100 ms: 1.29x faster                                                            |
| spectral_norm              | 110 ms                                                 | 86.6 ms: 1.27x faster                                                           |
| deepcopy_reduce            | 3.08 us                                                | 2.44 us: 1.26x faster                                                           |
| pathlib                    | 21.5 ms                                                | 17.1 ms: 1.26x faster                                                           |
| unpickle_pure_python       | 221 us                                                 | 176 us: 1.25x faster                                                            |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                           |
| pyflate                    | 448 ms                                                 | 364 ms: 1.23x faster                                                            |
| nbody                      | 89.3 ms                                                | 74.1 ms: 1.21x faster                                                           |
| chaos                      | 62.8 ms                                                | 52.5 ms: 1.20x faster                                                           |
| regex_compile              | 142 ms                                                 | 121 ms: 1.18x faster                                                            |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 83.0 ms: 1.17x faster                                                           |
| scimark_lu                 | 114 ms                                                 | 98.1 ms: 1.16x faster                                                           |
| crypto_pyaes               | 76.6 ms                                                | 66.5 ms: 1.15x faster                                                           |
| pprint_pformat             | 1.52 sec                                               | 1.32 sec: 1.15x faster                                                          |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                            |
| pprint_safe_repr           | 743 ms                                                 | 655 ms: 1.13x faster                                                            |
| logging_simple             | 6.63 us                                                | 5.92 us: 1.12x faster                                                           |
| pickle_pure_python         | 308 us                                                 | 276 us: 1.11x faster                                                            |
| thrift                     | 791 us                                                 | 718 us: 1.10x faster                                                            |
| logging_format             | 7.35 us                                                | 6.66 us: 1.10x faster                                                           |
| xml_etree_process          | 59.0 ms                                                | 53.8 ms: 1.10x faster                                                           |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                           |
| generators                 | 32.2 ms                                                | 29.6 ms: 1.09x faster                                                           |
| async_generators           | 384 ms                                                 | 353 ms: 1.09x faster                                                            |
| xml_etree_generate         | 85.2 ms                                                | 78.4 ms: 1.09x faster                                                           |
| json_dumps                 | 10.4 ms                                                | 9.55 ms: 1.08x faster                                                           |
| dulwich_log                | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                           |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                            |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                          |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                                            |
| fannkuch                   | 372 ms                                                 | 351 ms: 1.06x faster                                                            |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                          |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                            |
| mako                       | 11.0 ms                                                | 10.4 ms: 1.05x faster                                                           |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                                           |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                           |
| hexiom                     | 6.17 ms                                                | 6.02 ms: 1.02x faster                                                           |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                           |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                           |
| html5lib                   | 63.6 ms                                                | 64.6 ms: 1.02x slower                                                           |
| docutils                   | 2.64 sec                                               | 2.71 sec: 1.03x slower                                                          |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                           |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                            |
| sympy_sum                  | 166 ms                                                 | 171 ms: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.55 ms: 1.04x slower                                                           |
| sympy_str                  | 292 ms                                                 | 306 ms: 1.05x slower                                                            |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                           |
| nqueens                    | 80.1 ms                                                | 84.6 ms: 1.06x slower                                                           |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                           |
| genshi_xml                 | 50.2 ms                                                | 53.7 ms: 1.07x slower                                                           |
| sympy_expand               | 468 ms                                                 | 509 ms: 1.09x slower                                                            |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                            |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                           |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                           |
| gc_traversal               | 3.46 ms                                                | 4.70 ms: 1.36x slower                                                           |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.74x slower                                                           |
| bench_mp_pool              | 10.8 ms                                                | 238 ms: 22.06x slower                                                           |
| telco                      | 6.53 ms                                                | 161 ms: 24.63x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                                    |

Benchmark hidden because not significant (2): sqlite_synth, django_template
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260102-3.15.0a3+-884a7a7-JIT/bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.121x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x