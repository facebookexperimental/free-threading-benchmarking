# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 55892a4
- commit date: 2025-10-20
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                    |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 477 ms: 1.51x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 477 ms: 1.50x faster                                                    |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                    |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.5 ms: 1.29x faster                                                   |
| nbody          | 89.3 ms                                                | 92.0 ms: 1.03x slower                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.11x faster                                                    |
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                   |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                    |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                    |
| json_dumps           | 10.4 ms                                                | 8.74 ms: 1.19x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 52.7 ms: 1.12x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 77.2 ms: 1.10x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 298 us: 1.03x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 94.5 ms: 1.02x faster                                                   |
| json_loads           | 26.5 us                                                | 26.1 us: 1.02x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.44 ms: 1.04x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.8 ms: 1.29x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.7 ms: 1.16x faster                                                   |
| django_template | 34.7 ms                                                | 33.9 ms: 1.02x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 51.6 ms: 1.03x slower                                                   |
| mako            | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.06x faster                                                  |
| richards                   | 45.9 ms                                                | 24.2 ms: 1.90x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 22.0 us: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                    |
| richards_super             | 51.9 ms                                                | 28.8 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 477 ms: 1.51x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 477 ms: 1.50x faster                                                    |
| deepcopy                   | 352 us                                                 | 235 us: 1.50x faster                                                    |
| scimark_fft                | 342 ms                                                 | 242 ms: 1.41x faster                                                    |
| logging_silent             | 109 ns                                                 | 78.0 ns: 1.40x faster                                                   |
| comprehensions             | 19.8 us                                                | 14.6 us: 1.36x faster                                                   |
| spectral_norm              | 110 ms                                                 | 84.1 ms: 1.31x faster                                                   |
| scimark_sor                | 130 ms                                                 | 99.7 ms: 1.30x faster                                                   |
| float                      | 80.8 ms                                                | 62.5 ms: 1.29x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.46 us: 1.25x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.79 ms: 1.23x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 94.7 ms: 1.20x faster                                                   |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 57.0 ms: 1.20x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                    |
| chaos                      | 62.8 ms                                                | 52.7 ms: 1.19x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 8.74 ms: 1.19x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.18x faster                                                  |
| genshi_text                | 22.8 ms                                                | 19.7 ms: 1.16x faster                                                   |
| generators                 | 32.2 ms                                                | 27.8 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.82 ms: 1.15x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.6 ms: 1.15x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                    |
| pyflate                    | 448 ms                                                 | 395 ms: 1.13x faster                                                    |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                    |
| raytrace                   | 299 ms                                                 | 266 ms: 1.12x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 52.7 ms: 1.12x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                   |
| regex_compile              | 142 ms                                                 | 129 ms: 1.11x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 77.2 ms: 1.10x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 148 us: 1.10x faster                                                    |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 677 ms: 1.10x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.11 us: 1.08x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                   |
| thrift                     | 791 us                                                 | 737 us: 1.07x faster                                                    |
| logging_format             | 7.35 us                                                | 6.86 us: 1.07x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                    |
| sympy_str                  | 292 ms                                                 | 279 ms: 1.05x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 75.4 ms: 1.05x faster                                                   |
| fannkuch                   | 372 ms                                                 | 356 ms: 1.04x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.91 ms: 1.04x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.13 us: 1.03x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 298 us: 1.03x faster                                                    |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                   |
| django_template            | 34.7 ms                                                | 33.9 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 94.5 ms: 1.02x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                  |
| json_loads                 | 26.5 us                                                | 26.1 us: 1.02x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 80.6 ms: 1.01x slower                                                   |
| meteor_contest             | 104 ms                                                 | 106 ms: 1.02x slower                                                    |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.02x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 968 us: 1.03x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 51.6 ms: 1.03x slower                                                   |
| nbody                      | 89.3 ms                                                | 92.0 ms: 1.03x slower                                                   |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                   |
| coverage                   | 71.4 ms                                                | 74.1 ms: 1.04x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.44 ms: 1.04x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                    |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                    |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.8 ms: 1.29x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.48 ms: 1.30x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 2.03 ms: 1.86x slower                                                   |
| telco                      | 6.53 ms                                                | 154 ms: 23.63x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                            |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251020-3.15.0a1+-55892a4-CLANG,JIT/bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.22x