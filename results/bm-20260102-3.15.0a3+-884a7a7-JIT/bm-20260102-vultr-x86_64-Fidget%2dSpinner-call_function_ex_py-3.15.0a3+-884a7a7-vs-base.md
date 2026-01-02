# Results vs. base

- fork: Fidget-Spinner
- ref: call_function_ex_py
- machine: linux-x86_64
- commit hash: 884a7a7
- commit date: 2026-01-02
- overall geometric mean: 1.001x slower
- HPT reliability: 92.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 246 ms: 1.01x faster                                                            |
| docutils       | 2.69 sec                                                               | 2.71 sec: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization     | 304 ms                                                                 | 296 ms: 1.03x faster                                                            |
| async_tree_none_tg         | 243 ms                                                                 | 237 ms: 1.03x faster                                                            |
| async_generators           | 362 ms                                                                 | 353 ms: 1.02x faster                                                            |
| async_tree_memoization_tg  | 306 ms                                                                 | 299 ms: 1.02x faster                                                            |
| async_tree_none            | 243 ms                                                                 | 237 ms: 1.02x faster                                                            |
| async_tree_io_tg           | 588 ms                                                                 | 581 ms: 1.01x faster                                                            |
| coroutines                 | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                                           |
| async_tree_cpu_io_mixed    | 489 ms                                                                 | 501 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 503 ms: 1.03x slower                                                            |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (2): async_tree_io, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 75.3 ms                                                                | 74.1 ms: 1.02x faster                                                           |
| pidigits       | 192 ms                                                                 | 206 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_v8       | 21.2 ms                                                                | 21.7 ms: 1.03x slower                                                           |
| regex_dna      | 168 ms                                                                 | 173 ms: 1.03x slower                                                            |
| regex_effbot   | 2.56 ms                                                                | 2.70 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                    |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| xml_etree_process    | 54.7 ms                                                                | 53.8 ms: 1.02x faster                                                           |
| xml_etree_iterparse  | 84.0 ms                                                                | 83.0 ms: 1.01x faster                                                           |
| unpickle_pure_python | 178 us                                                                 | 176 us: 1.01x faster                                                            |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                            |
| pickle_pure_python   | 278 us                                                                 | 276 us: 1.01x faster                                                            |
| json_loads           | 28.1 us                                                                | 28.4 us: 1.01x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                    |

Benchmark hidden because not significant (3): xml_etree_generate, tomli_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                                | 7.36 ms: 1.00x slower                                                           |
| python_startup         | 12.5 ms                                                                | 12.6 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 21.2 ms                                                                | 20.9 ms: 1.02x faster                                                           |
| genshi_xml     | 52.1 ms                                                                | 53.7 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| deepcopy_reduce            | 2.60 us                                                                | 2.44 us: 1.06x faster                                                           |
| pathlib                    | 17.7 ms                                                                | 17.1 ms: 1.04x faster                                                           |
| async_tree_memoization     | 304 ms                                                                 | 296 ms: 1.03x faster                                                            |
| nqueens                    | 86.8 ms                                                                | 84.6 ms: 1.03x faster                                                           |
| async_tree_none_tg         | 243 ms                                                                 | 237 ms: 1.03x faster                                                            |
| scimark_monte_carlo        | 53.4 ms                                                                | 52.0 ms: 1.03x faster                                                           |
| async_generators           | 362 ms                                                                 | 353 ms: 1.02x faster                                                            |
| thrift                     | 734 us                                                                 | 718 us: 1.02x faster                                                            |
| async_tree_memoization_tg  | 306 ms                                                                 | 299 ms: 1.02x faster                                                            |
| async_tree_none            | 243 ms                                                                 | 237 ms: 1.02x faster                                                            |
| pycparser                  | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                          |
| deepcopy_memo              | 25.1 us                                                                | 24.6 us: 1.02x faster                                                           |
| raytrace                   | 267 ms                                                                 | 263 ms: 1.02x faster                                                            |
| xml_etree_process          | 54.7 ms                                                                | 53.8 ms: 1.02x faster                                                           |
| mdp                        | 1.37 sec                                                               | 1.35 sec: 1.02x faster                                                          |
| nbody                      | 75.3 ms                                                                | 74.1 ms: 1.02x faster                                                           |
| genshi_text                | 21.2 ms                                                                | 20.9 ms: 1.02x faster                                                           |
| logging_format             | 6.76 us                                                                | 6.66 us: 1.01x faster                                                           |
| chaos                      | 53.2 ms                                                                | 52.5 ms: 1.01x faster                                                           |
| telco                      | 163 ms                                                                 | 161 ms: 1.01x faster                                                            |
| sqlglot_v2_normalize       | 109 ms                                                                 | 107 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 84.0 ms                                                                | 83.0 ms: 1.01x faster                                                           |
| deepcopy                   | 244 us                                                                 | 241 us: 1.01x faster                                                            |
| hexiom                     | 6.09 ms                                                                | 6.02 ms: 1.01x faster                                                           |
| async_tree_io_tg           | 588 ms                                                                 | 581 ms: 1.01x faster                                                            |
| richards_super             | 21.7 ms                                                                | 21.5 ms: 1.01x faster                                                           |
| sqlglot_v2_optimize        | 54.2 ms                                                                | 53.7 ms: 1.01x faster                                                           |
| coroutines                 | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                                           |
| deltablue                  | 2.68 ms                                                                | 2.66 ms: 1.01x faster                                                           |
| k_core                     | 1.88 sec                                                               | 1.86 sec: 1.01x faster                                                          |
| unpickle_pure_python       | 178 us                                                                 | 176 us: 1.01x faster                                                            |
| crypto_pyaes               | 67.0 ms                                                                | 66.5 ms: 1.01x faster                                                           |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                            |
| 2to3                       | 248 ms                                                                 | 246 ms: 1.01x faster                                                            |
| pickle_pure_python         | 278 us                                                                 | 276 us: 1.01x faster                                                            |
| sympy_str                  | 309 ms                                                                 | 306 ms: 1.01x faster                                                            |
| connected_components       | 380 ms                                                                 | 378 ms: 1.01x faster                                                            |
| coverage                   | 82.1 ms                                                                | 81.6 ms: 1.01x faster                                                           |
| spectral_norm              | 87.1 ms                                                                | 86.6 ms: 1.01x faster                                                           |
| fannkuch                   | 352 ms                                                                 | 351 ms: 1.00x faster                                                            |
| python_startup_no_site     | 7.35 ms                                                                | 7.36 ms: 1.00x slower                                                           |
| python_startup             | 12.5 ms                                                                | 12.6 ms: 1.00x slower                                                           |
| scimark_fft                | 256 ms                                                                 | 257 ms: 1.00x slower                                                            |
| sympy_integrate            | 20.2 ms                                                                | 20.3 ms: 1.01x slower                                                           |
| logging_silent             | 82.1 ns                                                                | 82.6 ns: 1.01x slower                                                           |
| comprehensions             | 15.8 us                                                                | 15.9 us: 1.01x slower                                                           |
| docutils                   | 2.69 sec                                                               | 2.71 sec: 1.01x slower                                                          |
| bpe_tokeniser              | 4.02 sec                                                               | 4.04 sec: 1.01x slower                                                          |
| json_loads                 | 28.1 us                                                                | 28.4 us: 1.01x slower                                                           |
| sympy_sum                  | 169 ms                                                                 | 171 ms: 1.01x slower                                                            |
| shortest_path              | 425 ms                                                                 | 429 ms: 1.01x slower                                                            |
| create_gc_cycles           | 1.87 ms                                                                | 1.89 ms: 1.01x slower                                                           |
| dulwich_log                | 72.0 ms                                                                | 73.0 ms: 1.01x slower                                                           |
| json                       | 4.89 ms                                                                | 4.98 ms: 1.02x slower                                                           |
| many_optionals             | 976 us                                                                 | 997 us: 1.02x slower                                                            |
| meteor_contest             | 96.7 ms                                                                | 98.8 ms: 1.02x slower                                                           |
| generators                 | 28.9 ms                                                                | 29.6 ms: 1.02x slower                                                           |
| async_tree_cpu_io_mixed    | 489 ms                                                                 | 501 ms: 1.02x slower                                                            |
| regex_v8                   | 21.2 ms                                                                | 21.7 ms: 1.03x slower                                                           |
| richards                   | 17.7 ms                                                                | 18.2 ms: 1.03x slower                                                           |
| regex_dna                  | 168 ms                                                                 | 173 ms: 1.03x slower                                                            |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 503 ms: 1.03x slower                                                            |
| genshi_xml                 | 52.1 ms                                                                | 53.7 ms: 1.03x slower                                                           |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 4.55 ms: 1.04x slower                                                           |
| regex_effbot               | 2.56 ms                                                                | 2.70 ms: 1.05x slower                                                           |
| pidigits                   | 192 ms                                                                 | 206 ms: 1.07x slower                                                            |
| gc_traversal               | 4.07 ms                                                                | 4.70 ms: 1.16x slower                                                           |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (27): async_tree_io, sympy_expand, sqlglot_v2_parse, django_template, regex_compile, bench_thread_pool, xml_etree_generate, go, pprint_pformat, typing_runtime_protocols, float, scimark_sor, pylint, scimark_lu, mako, asyncio_websockets, subparsers, pyflate, sqlite_synth, logging_simple, tomli_loads, json_dumps, sqlglot_v2_transpile, sphinx, html5lib, pprint_safe_repr, bench_mp_pool

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 92.37% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x