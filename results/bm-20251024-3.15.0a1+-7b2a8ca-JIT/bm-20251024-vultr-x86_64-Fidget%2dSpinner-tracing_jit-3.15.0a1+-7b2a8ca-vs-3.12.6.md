# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7b2a8ca
- commit date: 2025-10-24
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| docutils       | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                  |
| html5lib       | 63.6 ms                                                | 71.7 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.77x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 635 ms: 1.75x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 320 ms: 1.73x faster                                                    |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                    |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 63.3 ms: 1.28x faster                                                   |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                   |
| regex_compile  | 142 ms                                                 | 128 ms: 1.11x faster                                                    |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                   |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.20x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.17x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.48 ms: 1.09x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 79.4 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 55.0 ms: 1.07x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.01x slower                                                    |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.30 ms: 1.02x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| mako            | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                   |
| django_template | 34.7 ms                                                | 36.2 ms: 1.04x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 52.5 ms: 1.05x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 22.4 ms: 2.05x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.23 sec: 1.97x faster                                                  |
| richards_super             | 51.9 ms                                                | 27.2 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.77x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 635 ms: 1.75x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 320 ms: 1.73x faster                                                    |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.72x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 23.9 us: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                    |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                    |
| scimark_fft                | 342 ms                                                 | 264 ms: 1.30x faster                                                    |
| spectral_norm              | 110 ms                                                 | 85.3 ms: 1.29x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                   |
| float                      | 80.8 ms                                                | 63.3 ms: 1.28x faster                                                   |
| logging_silent             | 109 ns                                                 | 86.7 ns: 1.26x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.20x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 3.99 sec: 1.19x faster                                                  |
| pyflate                    | 448 ms                                                 | 379 ms: 1.18x faster                                                    |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 65.0 ms: 1.18x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.17x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 59.8 ms: 1.15x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                   |
| go                         | 139 ms                                                 | 125 ms: 1.11x faster                                                    |
| regex_compile              | 142 ms                                                 | 128 ms: 1.11x faster                                                    |
| generators                 | 32.2 ms                                                | 29.1 ms: 1.11x faster                                                   |
| pylint                     | 319 ms                                                 | 289 ms: 1.10x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.48 ms: 1.09x faster                                                   |
| chaos                      | 62.8 ms                                                | 57.5 ms: 1.09x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.11 us: 1.08x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 79.4 ms: 1.07x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 73.5 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 55.0 ms: 1.07x faster                                                   |
| raytrace                   | 299 ms                                                 | 280 ms: 1.07x faster                                                    |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| logging_format             | 7.35 us                                                | 6.92 us: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                    |
| fannkuch                   | 372 ms                                                 | 355 ms: 1.05x faster                                                    |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.92 ms: 1.04x faster                                                   |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 768 us: 1.03x faster                                                    |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 20.2 ms: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 4.97 ms: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.01x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                   |
| sympy_str                  | 292 ms                                                 | 296 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.47 ms: 1.02x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.30 ms: 1.02x slower                                                   |
| django_template            | 34.7 ms                                                | 36.2 ms: 1.04x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 52.5 ms: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| nqueens                    | 80.1 ms                                                | 84.5 ms: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                   |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                    |
| sympy_expand               | 468 ms                                                 | 515 ms: 1.10x slower                                                    |
| html5lib                   | 63.6 ms                                                | 71.7 ms: 1.13x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                   |
| coverage                   | 71.4 ms                                                | 83.1 ms: 1.16x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.08 ms: 1.18x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                   |
| deltablue                  | 3.45 ms                                                | 4.69 ms: 1.36x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                   |
| telco                      | 6.53 ms                                                | 160 ms: 24.52x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (4): sympy_sum, coroutines, scimark_lu, nbody
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-7b2a8ca-JIT/bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x