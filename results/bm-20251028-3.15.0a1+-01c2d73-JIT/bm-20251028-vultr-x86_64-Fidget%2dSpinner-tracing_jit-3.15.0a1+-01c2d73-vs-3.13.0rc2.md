# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 01c2d73
- commit date: 2025-10-28
- overall geometric mean: 1.062x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                  |
| html5lib       | 67.0 ms                                                      | 68.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 557 ms: 1.57x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 589 ms: 1.55x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 488 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 482 ms: 1.32x faster                                                    |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                   |
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| Geometric mean | (ref)                                                        | 1.13x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                   |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                    |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 82.8 ms: 1.15x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 184 us: 1.14x faster                                                    |
| json_dumps           | 10.5 ms                                                      | 9.40 ms: 1.12x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 54.5 ms: 1.09x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 79.6 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 302 us: 1.03x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                   |
| genshi_xml     | 48.8 ms                                                      | 54.4 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                            |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 21.4 ms: 2.12x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.4 ms: 2.03x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 23.1 us: 1.69x faster                                                   |
| async_tree_io              | 876 ms                                                       | 557 ms: 1.57x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 589 ms: 1.55x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                    |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| scimark_sor                | 134 ms                                                       | 98.5 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 488 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                    |
| scimark_fft                | 349 ms                                                       | 261 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 482 ms: 1.32x faster                                                    |
| spectral_norm              | 111 ms                                                       | 84.5 ms: 1.31x faster                                                   |
| float                      | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                   |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                    |
| pyflate                    | 449 ms                                                       | 380 ms: 1.18x faster                                                    |
| logging_silent             | 103 ns                                                       | 86.9 ns: 1.18x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 82.8 ms: 1.15x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 184 us: 1.14x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.5 ms: 1.14x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.20 ms: 1.12x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.40 ms: 1.12x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 101 ms: 1.11x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.82 ms: 1.11x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.03 sec: 1.10x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 54.5 ms: 1.09x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                  |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 79.6 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.82 us: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.06x faster                                                   |
| chaos                      | 57.3 ms                                                      | 54.2 ms: 1.06x faster                                                   |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                    |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                    |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 710 ms: 1.04x faster                                                    |
| logging_format             | 6.84 us                                                      | 6.60 us: 1.04x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 72.4 ms: 1.03x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                   |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| meteor_contest             | 102 ms                                                       | 99.5 ms: 1.02x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.8 ms: 1.01x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                    |
| thrift                     | 778 us                                                       | 788 us: 1.01x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                   |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 68.5 ms: 1.02x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 302 us: 1.03x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.25 ms: 1.04x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.6 us: 1.06x slower                                                   |
| raytrace                   | 253 ms                                                       | 271 ms: 1.07x slower                                                    |
| sympy_sum                  | 156 ms                                                       | 167 ms: 1.08x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 85.5 ms: 1.09x slower                                                   |
| sympy_expand               | 457 ms                                                       | 501 ms: 1.10x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                   |
| sympy_str                  | 275 ms                                                       | 304 ms: 1.11x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 54.4 ms: 1.11x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.45x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.55 ms: 1.45x slower                                                   |
| telco                      | 7.82 ms                                                      | 164 ms: 20.93x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (7): pylint, crypto_pyaes, genshi_text, nbody, fannkuch, sqlite_synth, django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251028-3.15.0a1+-01c2d73-JIT/bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x