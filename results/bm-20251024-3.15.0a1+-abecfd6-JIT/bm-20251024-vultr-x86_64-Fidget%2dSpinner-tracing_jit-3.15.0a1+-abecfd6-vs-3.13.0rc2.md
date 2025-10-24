# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: abecfd6
- commit date: 2025-10-24
- overall geometric mean: 1.051x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                  |
| html5lib       | 67.0 ms                                                      | 69.3 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 562 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.47x faster                                                    |
| async_tree_none            | 354 ms                                                       | 251 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 512 ms: 1.25x faster                                                    |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 61.4 ms: 1.26x faster                                                   |
| pidigits       | 217 ms                                                       | 216 ms: 1.00x faster                                                    |
| nbody          | 85.1 ms                                                      | 93.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.50 ms: 1.23x faster                                                   |
| regex_dna      | 180 ms                                                       | 161 ms: 1.12x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                   |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                        | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.24 ms: 1.14x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 185 us: 1.13x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.9 ms: 1.13x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.12x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 55.7 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.23 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 53.0 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.5 ms: 2.01x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.24 sec: 1.90x faster                                                  |
| richards_super             | 51.6 ms                                                      | 27.5 ms: 1.88x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 24.0 us: 1.62x faster                                                   |
| async_tree_io              | 876 ms                                                       | 562 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.47x faster                                                    |
| deepcopy                   | 355 us                                                       | 252 us: 1.41x faster                                                    |
| async_tree_none            | 354 ms                                                       | 251 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                    |
| scimark_fft                | 349 ms                                                       | 260 ms: 1.34x faster                                                    |
| scimark_sor                | 134 ms                                                       | 100 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                    |
| spectral_norm              | 111 ms                                                       | 85.6 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                    |
| float                      | 77.5 ms                                                      | 61.4 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 512 ms: 1.25x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.50 ms: 1.23x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                   |
| logging_silent             | 103 ns                                                       | 86.6 ns: 1.18x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.24 ms: 1.14x faster                                                   |
| go                         | 141 ms                                                       | 124 ms: 1.13x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 185 us: 1.13x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.9 ms: 1.13x faster                                                   |
| pyflate                    | 449 ms                                                       | 397 ms: 1.13x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.9 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.19 ms: 1.12x faster                                                   |
| regex_dna                  | 180 ms                                                       | 161 ms: 1.12x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.12x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.04 sec: 1.10x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.84 ms: 1.10x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 104 ms: 1.08x faster                                                    |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 55.7 ms: 1.07x faster                                                   |
| pylint                     | 317 ms                                                       | 299 ms: 1.06x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| chaos                      | 57.3 ms                                                      | 54.3 ms: 1.06x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 64.5 ms: 1.05x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.23 ms: 1.02x faster                                                   |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                    |
| meteor_contest             | 102 ms                                                       | 99.5 ms: 1.02x faster                                                   |
| regex_compile              | 132 ms                                                       | 130 ms: 1.02x faster                                                    |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 74.2 ms: 1.01x faster                                                   |
| pidigits                   | 217 ms                                                       | 216 ms: 1.00x faster                                                    |
| fannkuch                   | 370 ms                                                       | 368 ms: 1.00x faster                                                    |
| thrift                     | 778 us                                                       | 787 us: 1.01x slower                                                    |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.06 ms: 1.01x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.27 us: 1.02x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.02 us: 1.03x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 69.3 ms: 1.03x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 162 ms: 1.04x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 161 us: 1.04x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.05x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                    |
| sympy_str                  | 275 ms                                                       | 293 ms: 1.07x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 20.4 ms: 1.07x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 53.0 ms: 1.09x slower                                                   |
| nbody                      | 85.1 ms                                                      | 93.1 ms: 1.09x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 86.3 ms: 1.10x slower                                                   |
| raytrace                   | 253 ms                                                       | 279 ms: 1.10x slower                                                    |
| sympy_expand               | 457 ms                                                       | 507 ms: 1.11x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.64 ms: 1.48x slower                                                   |
| telco                      | 7.82 ms                                                      | 159 ms: 20.35x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                            |

Benchmark hidden because not significant (3): genshi_text, sympy_integrate, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-abecfd6-JIT/bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x