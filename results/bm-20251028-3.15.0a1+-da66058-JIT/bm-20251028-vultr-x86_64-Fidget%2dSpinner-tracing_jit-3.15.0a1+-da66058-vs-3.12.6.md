# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: da66058
- commit date: 2025-10-28
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                  |
| html5lib       | 63.6 ms                                                | 68.9 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.94x faster                                                    |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 594 ms: 1.87x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 486 ms: 1.47x faster                                                    |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 546 ms: 1.06x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.0 ms: 1.35x faster                                                   |
| nbody          | 89.3 ms                                                | 86.5 ms: 1.03x faster                                                   |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                   |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                    |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                    |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 184 us: 1.20x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.55 ms: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 55.2 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 299 us: 1.03x faster                                                    |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                   |
| mako           | 11.0 ms                                                | 10.6 ms: 1.03x faster                                                   |
| genshi_xml     | 50.2 ms                                                | 53.7 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 21.2 ms: 2.17x faster                                                   |
| richards_super             | 51.9 ms                                                | 25.4 ms: 2.04x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.94x faster                                                    |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 594 ms: 1.87x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 23.3 us: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 486 ms: 1.47x faster                                                    |
| deepcopy                   | 352 us                                                 | 245 us: 1.44x faster                                                    |
| scimark_fft                | 342 ms                                                 | 253 ms: 1.35x faster                                                    |
| float                      | 80.8 ms                                                | 60.0 ms: 1.35x faster                                                   |
| scimark_sor                | 130 ms                                                 | 96.7 ms: 1.34x faster                                                   |
| spectral_norm              | 110 ms                                                 | 84.0 ms: 1.31x faster                                                   |
| logging_silent             | 109 ns                                                 | 88.1 ns: 1.24x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.84 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 184 us: 1.20x faster                                                    |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 57.3 ms: 1.19x faster                                                   |
| pyflate                    | 448 ms                                                 | 381 ms: 1.18x faster                                                    |
| chaos                      | 62.8 ms                                                | 53.6 ms: 1.17x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.1 ms: 1.16x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.76 us: 1.15x faster                                                   |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.14x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                   |
| logging_format             | 7.35 us                                                | 6.54 us: 1.12x faster                                                   |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                    |
| raytrace                   | 299 ms                                                 | 272 ms: 1.10x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 104 ms: 1.10x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.09x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.55 ms: 1.08x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 55.2 ms: 1.07x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 698 ms: 1.06x faster                                                    |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                    |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.23 ms: 1.04x faster                                                   |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.03x faster                                                   |
| nbody                      | 89.3 ms                                                | 86.5 ms: 1.03x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 299 us: 1.03x faster                                                    |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                    |
| fannkuch                   | 372 ms                                                 | 363 ms: 1.03x faster                                                    |
| json                       | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.27 ms: 1.02x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 169 ms: 1.02x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                   |
| sympy_str                  | 292 ms                                                 | 308 ms: 1.06x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 546 ms: 1.06x slower                                                    |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                    |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 53.7 ms: 1.07x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.08x slower                                                   |
| nqueens                    | 80.1 ms                                                | 86.3 ms: 1.08x slower                                                   |
| html5lib                   | 63.6 ms                                                | 68.9 ms: 1.08x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                   |
| sympy_expand               | 468 ms                                                 | 509 ms: 1.09x slower                                                    |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.40 ms: 1.27x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.76x slower                                                   |
| telco                      | 6.53 ms                                                | 163 ms: 24.91x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (5): pylint, thrift, django_template, coroutines, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251028-3.15.0a1+-da66058-JIT/bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x