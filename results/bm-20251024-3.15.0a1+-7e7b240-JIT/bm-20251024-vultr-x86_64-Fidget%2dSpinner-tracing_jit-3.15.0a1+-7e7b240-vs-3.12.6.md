# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7e7b240
- commit date: 2025-10-24
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                    |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                  |
| html5lib       | 63.6 ms                                                | 70.2 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 560 ms: 1.93x faster                                                    |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                    |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 61.9 ms: 1.30x faster                                                   |
| nbody          | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                   |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                   |
| regex_compile  | 142 ms                                                 | 131 ms: 1.09x faster                                                    |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                   |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 190 us: 1.16x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 83.3 ms: 1.16x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.55 ms: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 80.2 ms: 1.06x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 55.5 ms: 1.06x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                    |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.30 ms: 1.02x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.7 ms: 1.05x faster                                                   |
| mako            | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                   |
| django_template | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 53.7 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 22.5 ms: 2.04x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.23 sec: 1.96x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 560 ms: 1.93x faster                                                    |
| richards_super             | 51.9 ms                                                | 27.3 ms: 1.90x faster                                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 23.9 us: 1.68x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                    |
| deepcopy                   | 352 us                                                 | 256 us: 1.38x faster                                                    |
| scimark_sor                | 130 ms                                                 | 99.2 ms: 1.31x faster                                                   |
| float                      | 80.8 ms                                                | 61.9 ms: 1.30x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.3 us: 1.29x faster                                                   |
| spectral_norm              | 110 ms                                                 | 85.4 ms: 1.29x faster                                                   |
| scimark_fft                | 342 ms                                                 | 266 ms: 1.28x faster                                                    |
| logging_silent             | 109 ns                                                 | 88.2 ns: 1.24x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.83 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 57.9 ms: 1.18x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.4 ms: 1.17x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 190 us: 1.16x faster                                                    |
| pyflate                    | 448 ms                                                 | 385 ms: 1.16x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 83.3 ms: 1.16x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.4 ms: 1.16x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                   |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                    |
| generators                 | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 103 ms: 1.11x faster                                                    |
| regex_compile              | 142 ms                                                 | 131 ms: 1.09x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.55 ms: 1.08x faster                                                   |
| raytrace                   | 299 ms                                                 | 279 ms: 1.07x faster                                                    |
| pylint                     | 319 ms                                                 | 300 ms: 1.06x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 80.2 ms: 1.06x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 55.5 ms: 1.06x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 74.3 ms: 1.06x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.7 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 706 ms: 1.05x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.32 us: 1.05x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.04x faster                                                   |
| logging_format             | 7.35 us                                                | 7.08 us: 1.04x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.97 ms: 1.03x faster                                                   |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                    |
| thrift                     | 791 us                                                 | 768 us: 1.03x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                    |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                    |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 162 ms: 1.02x faster                                                    |
| mako                       | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                   |
| fannkuch                   | 372 ms                                                 | 368 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.36 ms: 1.01x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                   |
| sympy_str                  | 292 ms                                                 | 294 ms: 1.01x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.30 ms: 1.02x slower                                                   |
| nbody                      | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                   |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                    |
| django_template            | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 53.7 ms: 1.07x slower                                                   |
| nqueens                    | 80.1 ms                                                | 85.7 ms: 1.07x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                   |
| sympy_expand               | 468 ms                                                 | 509 ms: 1.09x slower                                                    |
| html5lib                   | 63.6 ms                                                | 70.2 ms: 1.10x slower                                                   |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.33 ms: 1.25x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.78x slower                                                   |
| telco                      | 6.53 ms                                                | 162 ms: 24.85x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-7e7b240-JIT/bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x