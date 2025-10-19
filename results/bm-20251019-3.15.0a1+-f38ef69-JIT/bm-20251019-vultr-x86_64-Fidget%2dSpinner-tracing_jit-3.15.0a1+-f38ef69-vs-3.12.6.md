# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f38ef69
- commit date: 2025-10-19
- overall geometric mean: 1.002x faster
- HPT reliability: 51.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 291 ms: 1.10x slower                                                    |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                  |
| html5lib       | 63.6 ms                                                | 75.1 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 344 ms: 1.63x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 675 ms: 1.60x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 696 ms: 1.60x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 281 ms: 1.59x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                    |
| async_tree_none            | 464 ms                                                 | 301 ms: 1.54x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 528 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                    |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| coroutines                 | 23.9 ms                                                | 27.5 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 63.5 ms: 1.27x faster                                                   |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                    |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                   |
| regex_compile  | 142 ms                                                 | 160 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 190 us: 1.16x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.33 ms: 1.11x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 87.9 ms: 1.03x slower                                                   |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 63.6 ms: 1.08x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.9 ms: 1.30x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                   |
| genshi_text     | 22.8 ms                                                | 24.9 ms: 1.09x slower                                                   |
| django_template | 34.7 ms                                                | 43.2 ms: 1.25x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 70.1 ms: 1.40x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| deepcopy_memo              | 40.3 us                                                | 23.2 us: 1.73x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.43 sec: 1.69x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 344 ms: 1.63x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 675 ms: 1.60x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 696 ms: 1.60x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 281 ms: 1.59x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                    |
| async_tree_none            | 464 ms                                                 | 301 ms: 1.54x faster                                                    |
| richards                   | 45.9 ms                                                | 30.4 ms: 1.51x faster                                                   |
| richards_super             | 51.9 ms                                                | 34.7 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 528 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                    |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                    |
| spectral_norm              | 110 ms                                                 | 84.1 ms: 1.31x faster                                                   |
| logging_silent             | 109 ns                                                 | 84.1 ns: 1.30x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                   |
| float                      | 80.8 ms                                                | 63.5 ms: 1.27x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                   |
| scimark_fft                | 342 ms                                                 | 279 ms: 1.22x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 3.97 sec: 1.19x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 190 us: 1.16x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 59.9 ms: 1.14x faster                                                   |
| pyflate                    | 448 ms                                                 | 393 ms: 1.14x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.05 ms: 1.13x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.33 ms: 1.11x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 69.3 ms: 1.11x faster                                                   |
| go                         | 139 ms                                                 | 131 ms: 1.06x faster                                                    |
| chaos                      | 62.8 ms                                                | 59.2 ms: 1.06x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.05x faster                                                    |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.8 ms: 1.03x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 76.4 ms: 1.03x faster                                                   |
| fannkuch                   | 372 ms                                                 | 362 ms: 1.03x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                   |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                                    |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                                    |
| raytrace                   | 299 ms                                                 | 308 ms: 1.03x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 87.9 ms: 1.03x slower                                                   |
| thrift                     | 791 us                                                 | 817 us: 1.03x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 768 ms: 1.03x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.57 sec: 1.03x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.3 ms: 1.04x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 173 ms: 1.04x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 171 us: 1.05x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                   |
| nqueens                    | 80.1 ms                                                | 84.1 ms: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.50 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.12 us: 1.07x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 63.6 ms: 1.08x slower                                                   |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.27 sec: 1.08x slower                                                  |
| logging_format             | 7.35 us                                                | 7.98 us: 1.09x slower                                                   |
| genshi_text                | 22.8 ms                                                | 24.9 ms: 1.09x slower                                                   |
| 2to3                       | 264 ms                                                 | 291 ms: 1.10x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.12x slower                                                    |
| regex_compile              | 142 ms                                                 | 160 ms: 1.12x slower                                                    |
| coroutines                 | 23.9 ms                                                | 27.5 ms: 1.15x slower                                                   |
| generators                 | 32.2 ms                                                | 37.2 ms: 1.15x slower                                                   |
| sympy_expand               | 468 ms                                                 | 540 ms: 1.16x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.16x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 12.7 ms: 1.18x slower                                                   |
| html5lib                   | 63.6 ms                                                | 75.1 ms: 1.18x slower                                                   |
| coverage                   | 71.4 ms                                                | 84.8 ms: 1.19x slower                                                   |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                    |
| django_template            | 34.7 ms                                                | 43.2 ms: 1.25x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.9 ms: 1.30x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.53 ms: 1.31x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 70.1 ms: 1.40x slower                                                   |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                   |
| telco                      | 6.53 ms                                                | 189 ms: 28.90x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (4): pylint, json, regex_dna, scimark_sparse_mat_mult
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251019-3.15.0a1+-f38ef69-JIT/bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 51.15% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.19x