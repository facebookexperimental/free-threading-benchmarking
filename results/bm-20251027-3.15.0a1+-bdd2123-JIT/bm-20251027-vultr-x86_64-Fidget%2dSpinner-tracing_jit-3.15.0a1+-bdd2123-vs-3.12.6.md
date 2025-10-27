# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: bdd2123
- commit date: 2025-10-27
- overall geometric mean: 1.083x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                  |
| html5lib       | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 563 ms: 1.92x faster                                                    |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                    |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 546 ms: 1.06x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.3 ms: 1.30x faster                                                   |
| nbody          | 89.3 ms                                                | 90.5 ms: 1.01x slower                                                   |
| pidigits       | 184 ms                                                 | 204 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                   |
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                                    |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| regex_v8       | 20.6 ms                                                | 22.1 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 186 us: 1.18x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 85.1 ms: 1.14x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.46 ms: 1.09x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 80.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 57.0 ms: 1.03x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 299 us: 1.03x faster                                                    |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.27 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| mako            | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                   |
| django_template | 34.7 ms                                                | 38.8 ms: 1.12x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 56.2 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.8 ms: 2.21x faster                                                   |
| richards_super             | 51.9 ms                                                | 25.2 ms: 2.06x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 563 ms: 1.92x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.27 sec: 1.90x faster                                                  |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 23.3 us: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                    |
| deepcopy                   | 352 us                                                 | 257 us: 1.37x faster                                                    |
| scimark_sor                | 130 ms                                                 | 97.0 ms: 1.34x faster                                                   |
| scimark_fft                | 342 ms                                                 | 260 ms: 1.31x faster                                                    |
| spectral_norm              | 110 ms                                                 | 84.8 ms: 1.30x faster                                                   |
| float                      | 80.8 ms                                                | 62.3 ms: 1.30x faster                                                   |
| logging_silent             | 109 ns                                                 | 86.8 ns: 1.26x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.84 ms: 1.21x faster                                                   |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 186 us: 1.18x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 57.9 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.06 sec: 1.17x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.3 ms: 1.16x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                  |
| pyflate                    | 448 ms                                                 | 393 ms: 1.14x faster                                                    |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 85.1 ms: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 103 ms: 1.11x faster                                                    |
| regex_compile              | 142 ms                                                 | 130 ms: 1.10x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.46 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 683 ms: 1.09x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.13 us: 1.08x faster                                                   |
| raytrace                   | 299 ms                                                 | 278 ms: 1.08x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 73.8 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 80.6 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                  |
| logging_format             | 7.35 us                                                | 7.05 us: 1.04x faster                                                   |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.22 ms: 1.04x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 57.0 ms: 1.03x faster                                                   |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 299 us: 1.03x faster                                                    |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                    |
| mako                       | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                   |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 161 us: 1.01x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                   |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 168 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                   |
| nbody                      | 89.3 ms                                                | 90.5 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.27 ms: 1.01x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.31 ms: 1.02x slower                                                   |
| sympy_str                  | 292 ms                                                 | 304 ms: 1.04x slower                                                    |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 546 ms: 1.06x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 22.1 ms: 1.08x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                   |
| nqueens                    | 80.1 ms                                                | 88.0 ms: 1.10x slower                                                   |
| html5lib                   | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                   |
| pidigits                   | 184 ms                                                 | 204 ms: 1.11x slower                                                    |
| sympy_expand               | 468 ms                                                 | 523 ms: 1.12x slower                                                    |
| django_template            | 34.7 ms                                                | 38.8 ms: 1.12x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 56.2 ms: 1.12x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.6 ms: 1.17x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.88 ms: 1.41x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                   |
| telco                      | 6.53 ms                                                | 163 ms: 25.03x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (4): pylint, coroutines, pycparser, thrift
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251027-3.15.0a1+-bdd2123-JIT/bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x