# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: a64215d
- commit date: 2025-11-06
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                  |
| html5lib       | 63.6 ms                                                | 68.9 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 559 ms: 1.94x faster                                                    |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                    |
| async_generators           | 384 ms                                                 | 361 ms: 1.06x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.7 ms: 1.33x faster                                                   |
| nbody          | 89.3 ms                                                | 84.0 ms: 1.06x faster                                                   |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                   |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                    |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.20x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 83.6 ms: 1.16x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.13 ms: 1.13x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 54.9 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 79.7 ms: 1.07x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 299 us: 1.03x faster                                                    |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                   |
| django_template | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 21.5 ms: 2.14x faster                                                   |
| richards_super             | 51.9 ms                                                | 25.8 ms: 2.01x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 559 ms: 1.94x faster                                                    |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 25.1 us: 1.61x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                    |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                    |
| scimark_sor                | 130 ms                                                 | 95.8 ms: 1.35x faster                                                   |
| go                         | 139 ms                                                 | 103 ms: 1.35x faster                                                    |
| scimark_fft                | 342 ms                                                 | 253 ms: 1.35x faster                                                    |
| float                      | 80.8 ms                                                | 60.7 ms: 1.33x faster                                                   |
| spectral_norm              | 110 ms                                                 | 83.6 ms: 1.32x faster                                                   |
| logging_silent             | 109 ns                                                 | 86.4 ns: 1.26x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 55.0 ms: 1.24x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.81 ms: 1.22x faster                                                   |
| pyflate                    | 448 ms                                                 | 367 ms: 1.22x faster                                                    |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.20x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.6 ms: 1.17x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                   |
| chaos                      | 62.8 ms                                                | 54.1 ms: 1.16x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 83.6 ms: 1.16x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.13 sec: 1.15x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.83 us: 1.14x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.13 ms: 1.13x faster                                                   |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                    |
| logging_format             | 7.35 us                                                | 6.53 us: 1.13x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 102 ms: 1.12x faster                                                    |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.03 ms: 1.09x faster                                                   |
| raytrace                   | 299 ms                                                 | 275 ms: 1.09x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 690 ms: 1.08x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 54.9 ms: 1.07x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 79.7 ms: 1.07x faster                                                   |
| async_generators           | 384 ms                                                 | 361 ms: 1.06x faster                                                    |
| nbody                      | 89.3 ms                                                | 84.0 ms: 1.06x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 75.0 ms: 1.05x faster                                                   |
| 2to3                       | 264 ms                                                 | 252 ms: 1.05x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                    |
| thrift                     | 791 us                                                 | 767 us: 1.03x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 299 us: 1.03x faster                                                    |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                    |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                                    |
| hexiom                     | 6.17 ms                                                | 6.09 ms: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 168 ms: 1.01x slower                                                    |
| django_template            | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                  |
| sympy_str                  | 292 ms                                                 | 306 ms: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                                   |
| nqueens                    | 80.1 ms                                                | 85.0 ms: 1.06x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                   |
| html5lib                   | 63.6 ms                                                | 68.9 ms: 1.08x slower                                                   |
| sympy_expand               | 468 ms                                                 | 508 ms: 1.09x slower                                                    |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                   |
| coverage                   | 71.4 ms                                                | 80.9 ms: 1.13x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.6 ms: 1.17x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.78 ms: 1.38x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.95 ms: 1.79x slower                                                   |
| telco                      | 6.53 ms                                                | 162 ms: 24.79x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                            |

Benchmark hidden because not significant (2): pylint, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251106-3.15.0a1+-a64215d-JIT/bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x