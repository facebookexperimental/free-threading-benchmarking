# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: call_function_ex_py
- machine: linux-x86_64
- commit hash: 884a7a7
- commit date: 2026-01-02
- overall geometric mean: 1.083x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 246 ms: 1.05x faster                                                            |
| docutils       | 2.62 sec                                                     | 2.71 sec: 1.04x slower                                                          |
| html5lib       | 67.0 ms                                                      | 64.6 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                            |
| async_tree_io_tg           | 913 ms                                                       | 581 ms: 1.57x faster                                                            |
| async_tree_memoization     | 461 ms                                                       | 296 ms: 1.56x faster                                                            |
| async_tree_none            | 354 ms                                                       | 237 ms: 1.49x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 237 ms: 1.42x faster                                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 501 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 503 ms: 1.27x faster                                                            |
| async_generators           | 377 ms                                                       | 353 ms: 1.07x faster                                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                           |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 57.6 ms: 1.34x faster                                                           |
| nbody          | 85.1 ms                                                      | 74.1 ms: 1.15x faster                                                           |
| pidigits       | 217 ms                                                       | 206 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                        | 1.17x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                           |
| regex_compile  | 132 ms                                                       | 121 ms: 1.09x faster                                                            |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                           |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 176 us: 1.19x faster                                                            |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.0 ms: 1.14x faster                                                           |
| json_dumps           | 10.5 ms                                                      | 9.55 ms: 1.10x faster                                                           |
| xml_etree_process    | 59.3 ms                                                      | 53.8 ms: 1.10x faster                                                           |
| xml_etree_generate   | 85.4 ms                                                      | 78.4 ms: 1.09x faster                                                           |
| pickle_pure_python   | 294 us                                                       | 276 us: 1.07x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                            |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                          |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                           |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                           |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                           |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.4 ms: 1.09x faster                                                           |
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                           |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                           |
| genshi_xml      | 48.8 ms                                                      | 53.7 ms: 1.10x slower                                                           |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.2 ms: 2.49x faster                                                           |
| richards_super             | 51.6 ms                                                      | 21.5 ms: 2.41x faster                                                           |
| mdp                        | 2.36 sec                                                     | 1.35 sec: 1.75x faster                                                          |
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                            |
| deepcopy_memo              | 39.1 us                                                      | 24.6 us: 1.59x faster                                                           |
| async_tree_io_tg           | 913 ms                                                       | 581 ms: 1.57x faster                                                            |
| async_tree_memoization     | 461 ms                                                       | 296 ms: 1.56x faster                                                            |
| go                         | 141 ms                                                       | 91.5 ms: 1.54x faster                                                           |
| async_tree_none            | 354 ms                                                       | 237 ms: 1.49x faster                                                            |
| deepcopy                   | 355 us                                                       | 241 us: 1.47x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 237 ms: 1.42x faster                                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.39x faster                                                            |
| scimark_fft                | 349 ms                                                       | 257 ms: 1.36x faster                                                            |
| float                      | 77.5 ms                                                      | 57.6 ms: 1.34x faster                                                           |
| scimark_sor                | 134 ms                                                       | 100 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 501 ms: 1.33x faster                                                            |
| spectral_norm              | 111 ms                                                       | 86.6 ms: 1.28x faster                                                           |
| deepcopy_reduce            | 3.11 us                                                      | 2.44 us: 1.27x faster                                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 503 ms: 1.27x faster                                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.0 ms: 1.26x faster                                                           |
| logging_silent             | 103 ns                                                       | 82.6 ns: 1.24x faster                                                           |
| pyflate                    | 449 ms                                                       | 364 ms: 1.23x faster                                                            |
| unpickle_pure_python       | 210 us                                                       | 176 us: 1.19x faster                                                            |
| deltablue                  | 3.12 ms                                                      | 2.66 ms: 1.18x faster                                                           |
| nbody                      | 85.1 ms                                                      | 74.1 ms: 1.15x faster                                                           |
| scimark_lu                 | 113 ms                                                       | 98.1 ms: 1.15x faster                                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.0 ms: 1.14x faster                                                           |
| regex_effbot               | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                           |
| pprint_pformat             | 1.50 sec                                                     | 1.32 sec: 1.13x faster                                                          |
| pprint_safe_repr           | 738 ms                                                       | 655 ms: 1.13x faster                                                            |
| pathlib                    | 19.2 ms                                                      | 17.1 ms: 1.12x faster                                                           |
| json_dumps                 | 10.5 ms                                                      | 9.55 ms: 1.10x faster                                                           |
| xml_etree_process          | 59.3 ms                                                      | 53.8 ms: 1.10x faster                                                           |
| bpe_tokeniser              | 4.45 sec                                                     | 4.04 sec: 1.10x faster                                                          |
| regex_compile              | 132 ms                                                       | 121 ms: 1.09x faster                                                            |
| chaos                      | 57.3 ms                                                      | 52.5 ms: 1.09x faster                                                           |
| xml_etree_generate         | 85.4 ms                                                      | 78.4 ms: 1.09x faster                                                           |
| mako                       | 11.3 ms                                                      | 10.4 ms: 1.09x faster                                                           |
| thrift                     | 778 us                                                       | 718 us: 1.08x faster                                                            |
| async_generators           | 377 ms                                                       | 353 ms: 1.07x faster                                                            |
| pickle_pure_python         | 294 us                                                       | 276 us: 1.07x faster                                                            |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                            |
| fannkuch                   | 370 ms                                                       | 351 ms: 1.05x faster                                                            |
| 2to3                       | 260 ms                                                       | 246 ms: 1.05x faster                                                            |
| pidigits                   | 217 ms                                                       | 206 ms: 1.05x faster                                                            |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                           |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                            |
| logging_simple             | 6.16 us                                                      | 5.92 us: 1.04x faster                                                           |
| html5lib                   | 67.0 ms                                                      | 64.6 ms: 1.04x faster                                                           |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.04x faster                                                           |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.55 ms: 1.03x faster                                                           |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                           |
| meteor_contest             | 102 ms                                                       | 98.8 ms: 1.03x faster                                                           |
| logging_format             | 6.84 us                                                      | 6.66 us: 1.03x faster                                                           |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                          |
| dulwich_log                | 74.8 ms                                                      | 73.0 ms: 1.02x faster                                                           |
| crypto_pyaes               | 67.9 ms                                                      | 66.5 ms: 1.02x faster                                                           |
| coverage                   | 83.0 ms                                                      | 81.6 ms: 1.02x faster                                                           |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                           |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                          |
| python_startup_no_site     | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                           |
| hexiom                     | 5.99 ms                                                      | 6.02 ms: 1.00x slower                                                           |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                           |
| django_template            | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                           |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.02x slower                                                           |
| generators                 | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                           |
| docutils                   | 2.62 sec                                                     | 2.71 sec: 1.04x slower                                                          |
| raytrace                   | 253 ms                                                       | 263 ms: 1.04x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                            |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                           |
| nqueens                    | 78.6 ms                                                      | 84.6 ms: 1.08x slower                                                           |
| sympy_sum                  | 156 ms                                                       | 171 ms: 1.10x slower                                                            |
| genshi_xml                 | 48.8 ms                                                      | 53.7 ms: 1.10x slower                                                           |
| sympy_expand               | 457 ms                                                       | 509 ms: 1.11x slower                                                            |
| sympy_str                  | 275 ms                                                       | 306 ms: 1.12x slower                                                            |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                           |
| create_gc_cycles           | 1.34 ms                                                      | 1.89 ms: 1.42x slower                                                           |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                           |
| gc_traversal               | 3.14 ms                                                      | 4.70 ms: 1.50x slower                                                           |
| telco                      | 7.82 ms                                                      | 161 ms: 20.55x slower                                                           |
| bench_mp_pool              | 11.0 ms                                                      | 238 ms: 21.66x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                                    |

Benchmark hidden because not significant (3): pylint, sqlite_synth, typing_runtime_protocols
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260102-3.15.0a3+-884a7a7-JIT/bm-20260102-vultr-x86_64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x