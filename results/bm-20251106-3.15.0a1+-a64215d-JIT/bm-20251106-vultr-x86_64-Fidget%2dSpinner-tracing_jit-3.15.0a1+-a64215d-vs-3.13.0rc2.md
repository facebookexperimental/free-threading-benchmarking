# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: a64215d
- commit date: 2025-11-06
- overall geometric mean: 1.063x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                  |
| html5lib       | 67.0 ms                                                      | 68.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 559 ms: 1.57x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 596 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 490 ms: 1.30x faster                                                    |
| async_generators           | 377 ms                                                       | 361 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.7 ms: 1.28x faster                                                   |
| pidigits       | 217 ms                                                       | 200 ms: 1.08x faster                                                    |
| nbody          | 85.1 ms                                                      | 84.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                        | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                   |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                   |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.13 ms: 1.15x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 183 us: 1.15x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.6 ms: 1.13x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 54.9 ms: 1.08x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 79.7 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 299 us: 1.01x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 55.1 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 21.5 ms: 2.11x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.8 ms: 2.00x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                  |
| async_tree_io              | 876 ms                                                       | 559 ms: 1.57x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 25.1 us: 1.56x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 596 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                    |
| scimark_sor                | 134 ms                                                       | 95.8 ms: 1.40x faster                                                   |
| scimark_fft                | 349 ms                                                       | 253 ms: 1.38x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                    |
| spectral_norm              | 111 ms                                                       | 83.6 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 490 ms: 1.30x faster                                                    |
| float                      | 77.5 ms                                                      | 60.7 ms: 1.28x faster                                                   |
| pyflate                    | 449 ms                                                       | 367 ms: 1.22x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.0 ms: 1.19x faster                                                   |
| logging_silent             | 103 ns                                                       | 86.4 ns: 1.19x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.18x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.03 ms: 1.17x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.13 ms: 1.15x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 183 us: 1.15x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.6 ms: 1.13x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 2.81 ms: 1.11x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 102 ms: 1.10x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| pidigits                   | 217 ms                                                       | 200 ms: 1.08x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 54.9 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.13 sec: 1.08x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 79.7 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 690 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.1 ms: 1.06x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.83 us: 1.06x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.53 us: 1.05x faster                                                   |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                   |
| async_generators           | 377 ms                                                       | 361 ms: 1.04x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 65.6 ms: 1.03x faster                                                   |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                    |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                   |
| coverage                   | 83.0 ms                                                      | 80.9 ms: 1.03x faster                                                   |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                   |
| thrift                     | 778 us                                                       | 767 us: 1.01x faster                                                    |
| nbody                      | 85.1 ms                                                      | 84.0 ms: 1.01x faster                                                   |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                                    |
| json                       | 4.93 ms                                                      | 4.96 ms: 1.01x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 299 us: 1.01x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 6.09 ms: 1.02x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.02x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 68.9 ms: 1.03x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 168 ms: 1.08x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 85.0 ms: 1.08x slower                                                   |
| raytrace                   | 253 ms                                                       | 275 ms: 1.09x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.10x slower                                                   |
| sympy_expand               | 457 ms                                                       | 508 ms: 1.11x slower                                                    |
| sympy_str                  | 275 ms                                                       | 306 ms: 1.11x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 55.1 ms: 1.13x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.95 ms: 1.46x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.78 ms: 1.52x slower                                                   |
| telco                      | 7.82 ms                                                      | 162 ms: 20.68x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (7): pylint, meteor_contest, genshi_text, sqlite_synth, pycparser, dulwich_log, generators
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251106-3.15.0a1+-a64215d-JIT/bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x