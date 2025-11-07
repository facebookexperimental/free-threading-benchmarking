# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: d47bed2
- commit date: 2025-11-06
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                             |
| html5lib       | 63.6 ms                                                | 68.0 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 566 ms: 1.91x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                             |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 489 ms: 1.46x faster                                                             |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                                             |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                                     |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 61.6 ms: 1.31x faster                                                            |
| nbody          | 89.3 ms                                                | 72.7 ms: 1.23x faster                                                            |
| pidigits       | 184 ms                                                 | 207 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                             |
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                            |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                            |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                             |
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                           |
| xml_etree_iterparse  | 96.7 ms                                                | 83.9 ms: 1.15x faster                                                            |
| json_dumps           | 10.4 ms                                                | 9.09 ms: 1.14x faster                                                            |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                             |
| xml_etree_process    | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                            |
| xml_etree_generate   | 85.2 ms                                                | 80.8 ms: 1.05x faster                                                            |
| pickle_pure_python   | 308 us                                                 | 299 us: 1.03x faster                                                             |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                            |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                            |
| mako            | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                            |
| django_template | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                            |
| genshi_xml      | 50.2 ms                                                | 55.0 ms: 1.10x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.3 ms: 2.27x faster                                                            |
| richards_super             | 51.9 ms                                                | 24.3 ms: 2.13x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 566 ms: 1.91x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                             |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                             |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                             |
| deepcopy_memo              | 40.3 us                                                | 25.6 us: 1.57x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 489 ms: 1.46x faster                                                             |
| deepcopy                   | 352 us                                                 | 254 us: 1.38x faster                                                             |
| go                         | 139 ms                                                 | 101 ms: 1.37x faster                                                             |
| scimark_fft                | 342 ms                                                 | 254 ms: 1.34x faster                                                             |
| scimark_sor                | 130 ms                                                 | 98.2 ms: 1.32x faster                                                            |
| float                      | 80.8 ms                                                | 61.6 ms: 1.31x faster                                                            |
| spectral_norm              | 110 ms                                                 | 87.8 ms: 1.25x faster                                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 55.0 ms: 1.25x faster                                                            |
| logging_silent             | 109 ns                                                 | 88.1 ns: 1.24x faster                                                            |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                            |
| nbody                      | 89.3 ms                                                | 72.7 ms: 1.23x faster                                                            |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                            |
| deltablue                  | 3.45 ms                                                | 2.87 ms: 1.20x faster                                                            |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                             |
| pyflate                    | 448 ms                                                 | 378 ms: 1.19x faster                                                             |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                           |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                            |
| chaos                      | 62.8 ms                                                | 53.7 ms: 1.17x faster                                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.07 sec: 1.16x faster                                                           |
| logging_simple             | 6.63 us                                                | 5.71 us: 1.16x faster                                                            |
| xml_etree_iterparse        | 96.7 ms                                                | 83.9 ms: 1.15x faster                                                            |
| logging_format             | 7.35 us                                                | 6.45 us: 1.14x faster                                                            |
| json_dumps                 | 10.4 ms                                                | 9.09 ms: 1.14x faster                                                            |
| crypto_pyaes               | 76.6 ms                                                | 67.3 ms: 1.14x faster                                                            |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                             |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                            |
| raytrace                   | 299 ms                                                 | 271 ms: 1.10x faster                                                             |
| scimark_lu                 | 114 ms                                                 | 104 ms: 1.10x faster                                                             |
| generators                 | 32.2 ms                                                | 29.6 ms: 1.09x faster                                                            |
| pprint_safe_repr           | 743 ms                                                 | 690 ms: 1.08x faster                                                             |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                             |
| xml_etree_process          | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                            |
| genshi_text                | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                            |
| xml_etree_generate         | 85.2 ms                                                | 80.8 ms: 1.05x faster                                                            |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.05x faster                                                           |
| dulwich_log                | 78.9 ms                                                | 74.9 ms: 1.05x faster                                                            |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                                             |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                             |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                             |
| pickle_pure_python         | 308 us                                                 | 299 us: 1.03x faster                                                             |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                             |
| mako                       | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.33 ms: 1.02x faster                                                            |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.01x faster                                                             |
| sympy_integrate            | 20.5 ms                                                | 20.4 ms: 1.01x faster                                                            |
| sympy_sum                  | 166 ms                                                 | 169 ms: 1.02x slower                                                             |
| django_template            | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                            |
| python_startup_no_site     | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                            |
| sympy_str                  | 292 ms                                                 | 306 ms: 1.05x slower                                                             |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                             |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                            |
| html5lib                   | 63.6 ms                                                | 68.0 ms: 1.07x slower                                                            |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.08x slower                                                            |
| nqueens                    | 80.1 ms                                                | 86.2 ms: 1.08x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                            |
| sympy_expand               | 468 ms                                                 | 508 ms: 1.09x slower                                                             |
| genshi_xml                 | 50.2 ms                                                | 55.0 ms: 1.10x slower                                                            |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                             |
| pidigits                   | 184 ms                                                 | 207 ms: 1.13x slower                                                             |
| bench_mp_pool              | 10.8 ms                                                | 12.6 ms: 1.17x slower                                                            |
| coverage                   | 71.4 ms                                                | 87.9 ms: 1.23x slower                                                            |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                            |
| gc_traversal               | 3.46 ms                                                | 4.55 ms: 1.32x slower                                                            |
| create_gc_cycles           | 1.09 ms                                                | 1.95 ms: 1.79x slower                                                            |
| telco                      | 6.53 ms                                                | 162 ms: 24.84x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                                     |

Benchmark hidden because not significant (6): pylint, thrift, sqlite_synth, coroutines, json, hexiom
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251106-3.15.0a1+-d47bed2-JIT/bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x