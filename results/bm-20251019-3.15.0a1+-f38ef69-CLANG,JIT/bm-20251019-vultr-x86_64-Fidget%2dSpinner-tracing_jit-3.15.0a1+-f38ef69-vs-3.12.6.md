# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f38ef69
- commit date: 2025-10-19
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 595 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                    |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 472 ms: 1.52x faster                                                    |
| async_generators           | 384 ms                                                 | 332 ms: 1.16x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.6 ms: 1.29x faster                                                   |
| nbody          | 89.3 ms                                                | 90.2 ms: 1.01x slower                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.10 ms: 1.02x faster                                                   |
| regex_compile  | 142 ms                                                 | 140 ms: 1.02x faster                                                    |
| regex_v8       | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                   |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                    |
| json_dumps           | 10.4 ms                                                | 8.71 ms: 1.19x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.81 sec: 1.16x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 54.7 ms: 1.08x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 80.2 ms: 1.06x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 293 us: 1.05x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 93.6 ms: 1.03x faster                                                   |
| json_loads           | 26.5 us                                                | 25.9 us: 1.03x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                   |
| django_template | 34.7 ms                                                | 34.0 ms: 1.02x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 57.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.22 sec: 1.99x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 21.7 us: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 595 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                    |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                    |
| richards                   | 45.9 ms                                                | 28.8 ms: 1.59x faster                                                   |
| richards_super             | 51.9 ms                                                | 33.6 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 472 ms: 1.52x faster                                                    |
| deepcopy                   | 352 us                                                 | 232 us: 1.51x faster                                                    |
| logging_silent             | 109 ns                                                 | 79.6 ns: 1.37x faster                                                   |
| scimark_fft                | 342 ms                                                 | 250 ms: 1.37x faster                                                    |
| comprehensions             | 19.8 us                                                | 14.7 us: 1.35x faster                                                   |
| spectral_norm              | 110 ms                                                 | 82.4 ms: 1.34x faster                                                   |
| scimark_sor                | 130 ms                                                 | 99.9 ms: 1.30x faster                                                   |
| float                      | 80.8 ms                                                | 62.6 ms: 1.29x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.40 us: 1.28x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.77 ms: 1.24x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 3.91 sec: 1.21x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 57.5 ms: 1.19x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 8.71 ms: 1.19x faster                                                   |
| chaos                      | 62.8 ms                                                | 53.5 ms: 1.18x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.5 ms: 1.17x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.81 sec: 1.16x faster                                                  |
| async_generators           | 384 ms                                                 | 332 ms: 1.16x faster                                                    |
| logging_simple             | 6.63 us                                                | 5.79 us: 1.15x faster                                                   |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                    |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 654 ms: 1.14x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                   |
| logging_format             | 7.35 us                                                | 6.49 us: 1.13x faster                                                   |
| pyflate                    | 448 ms                                                 | 396 ms: 1.13x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 145 us: 1.13x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 102 ms: 1.12x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.37 sec: 1.11x faster                                                  |
| raytrace                   | 299 ms                                                 | 269 ms: 1.11x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.03 ms: 1.09x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 54.7 ms: 1.08x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 73.2 ms: 1.08x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.80 ms: 1.06x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 80.2 ms: 1.06x faster                                                   |
| thrift                     | 791 us                                                 | 747 us: 1.06x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 293 us: 1.05x faster                                                    |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                    |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                    |
| fannkuch                   | 372 ms                                                 | 356 ms: 1.04x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 93.6 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                   |
| json_loads                 | 26.5 us                                                | 25.9 us: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.10 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                   |
| regex_compile              | 142 ms                                                 | 140 ms: 1.02x faster                                                    |
| django_template            | 34.7 ms                                                | 34.0 ms: 1.02x faster                                                   |
| nqueens                    | 80.1 ms                                                | 79.5 ms: 1.01x faster                                                   |
| sympy_expand               | 468 ms                                                 | 471 ms: 1.01x slower                                                    |
| nbody                      | 89.3 ms                                                | 90.2 ms: 1.01x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 966 us: 1.03x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                    |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| coverage                   | 71.4 ms                                                | 76.2 ms: 1.07x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                   |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                    |
| generators                 | 32.2 ms                                                | 36.2 ms: 1.12x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.3 ms: 1.14x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 57.7 ms: 1.15x slower                                                   |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                    |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.27x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.48 ms: 1.30x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 2.02 ms: 1.85x slower                                                   |
| telco                      | 6.53 ms                                                | 157 ms: 24.06x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                            |

Benchmark hidden because not significant (2): mako, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251019-3.15.0a1+-f38ef69-CLANG,JIT/bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.22x