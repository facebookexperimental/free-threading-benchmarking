# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: abecfd6
- commit date: 2025-10-24
- overall geometric mean: 1.087x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                    |
| docutils       | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                  |
| html5lib       | 63.6 ms                                                | 69.3 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 562 ms: 1.93x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_none            | 464 ms                                                 | 251 ms: 1.85x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.38x faster                                                    |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 61.4 ms: 1.32x faster                                                   |
| nbody          | 89.3 ms                                                | 93.1 ms: 1.04x slower                                                   |
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.50 ms: 1.27x faster                                                   |
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                                    |
| regex_dna      | 168 ms                                                 | 161 ms: 1.04x faster                                                    |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 83.9 ms: 1.15x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.24 ms: 1.12x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 55.7 ms: 1.06x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                                    |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.23 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| mako            | 11.0 ms                                                | 10.5 ms: 1.04x faster                                                   |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 53.0 ms: 1.06x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 22.5 ms: 2.05x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.24 sec: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 562 ms: 1.93x faster                                                    |
| richards_super             | 51.9 ms                                                | 27.5 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_none            | 464 ms                                                 | 251 ms: 1.85x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 24.0 us: 1.68x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                    |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.38x faster                                                    |
| float                      | 80.8 ms                                                | 61.4 ms: 1.32x faster                                                   |
| scimark_fft                | 342 ms                                                 | 260 ms: 1.31x faster                                                    |
| scimark_sor                | 130 ms                                                 | 100 ms: 1.30x faster                                                    |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                   |
| spectral_norm              | 110 ms                                                 | 85.6 ms: 1.29x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.50 ms: 1.27x faster                                                   |
| logging_silent             | 109 ns                                                 | 86.6 ns: 1.26x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.84 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 64.5 ms: 1.19x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 57.9 ms: 1.18x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.3 ms: 1.16x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 83.9 ms: 1.15x faster                                                   |
| pyflate                    | 448 ms                                                 | 397 ms: 1.13x faster                                                    |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.24 ms: 1.12x faster                                                   |
| regex_compile              | 142 ms                                                 | 130 ms: 1.10x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 104 ms: 1.09x faster                                                    |
| generators                 | 32.2 ms                                                | 29.6 ms: 1.09x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| raytrace                   | 299 ms                                                 | 279 ms: 1.07x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                   |
| pylint                     | 319 ms                                                 | 299 ms: 1.06x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 74.2 ms: 1.06x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 55.7 ms: 1.06x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.27 us: 1.06x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.19 ms: 1.05x faster                                                   |
| logging_format             | 7.35 us                                                | 7.02 us: 1.05x faster                                                   |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.04x faster                                                   |
| regex_dna                  | 168 ms                                                 | 161 ms: 1.04x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.5 ms: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                   |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                    |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 162 ms: 1.03x faster                                                    |
| hexiom                     | 6.17 ms                                                | 6.06 ms: 1.02x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 161 us: 1.01x faster                                                    |
| fannkuch                   | 372 ms                                                 | 368 ms: 1.01x faster                                                    |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.23 ms: 1.01x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                    |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                   |
| nbody                      | 89.3 ms                                                | 93.1 ms: 1.04x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 53.0 ms: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                   |
| nqueens                    | 80.1 ms                                                | 86.3 ms: 1.08x slower                                                   |
| sympy_expand               | 468 ms                                                 | 507 ms: 1.08x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.3 ms: 1.09x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.15x slower                                                   |
| pidigits                   | 184 ms                                                 | 216 ms: 1.17x slower                                                    |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.64 ms: 1.34x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.91 ms: 1.75x slower                                                   |
| telco                      | 6.53 ms                                                | 159 ms: 24.39x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (4): thrift, sympy_str, pycparser, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-abecfd6-JIT/bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x