# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: 7be738d
- commit date: 2025-10-28
- overall geometric mean: 1.104x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                             |
| html5lib       | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                             |
| async_tree_none            | 464 ms                                                 | 249 ms: 1.87x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                             |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                             |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                            |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.5 ms: 1.34x faster                                                            |
| nbody          | 89.3 ms                                                | 73.5 ms: 1.21x faster                                                            |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.55 ms: 1.24x faster                                                            |
| regex_compile  | 142 ms                                                 | 127 ms: 1.13x faster                                                             |
| regex_dna      | 168 ms                                                 | 168 ms: 1.00x slower                                                             |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.07x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 184 us: 1.20x faster                                                             |
| tomli_loads          | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                           |
| xml_etree_iterparse  | 96.7 ms                                                | 83.7 ms: 1.16x faster                                                            |
| json_dumps           | 10.4 ms                                                | 9.48 ms: 1.09x faster                                                            |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                             |
| xml_etree_process    | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                            |
| xml_etree_generate   | 85.2 ms                                                | 81.0 ms: 1.05x faster                                                            |
| pickle_pure_python   | 308 us                                                 | 296 us: 1.04x faster                                                             |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                            |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                            |
| mako           | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                            |
| genshi_xml     | 50.2 ms                                                | 54.0 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.0 ms: 2.29x faster                                                            |
| richards_super             | 51.9 ms                                                | 24.0 ms: 2.16x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                             |
| async_tree_none            | 464 ms                                                 | 249 ms: 1.87x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                             |
| mdp                        | 2.42 sec                                               | 1.35 sec: 1.80x faster                                                           |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                             |
| deepcopy_memo              | 40.3 us                                                | 23.7 us: 1.70x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                             |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                             |
| float                      | 80.8 ms                                                | 60.5 ms: 1.34x faster                                                            |
| scimark_sor                | 130 ms                                                 | 97.2 ms: 1.33x faster                                                            |
| scimark_fft                | 342 ms                                                 | 261 ms: 1.31x faster                                                             |
| spectral_norm              | 110 ms                                                 | 87.0 ms: 1.27x faster                                                            |
| logging_silent             | 109 ns                                                 | 86.7 ns: 1.26x faster                                                            |
| regex_effbot               | 3.17 ms                                                | 2.55 ms: 1.24x faster                                                            |
| deltablue                  | 3.45 ms                                                | 2.78 ms: 1.24x faster                                                            |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                            |
| nbody                      | 89.3 ms                                                | 73.5 ms: 1.21x faster                                                            |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 56.5 ms: 1.21x faster                                                            |
| comprehensions             | 19.8 us                                                | 16.4 us: 1.21x faster                                                            |
| unpickle_pure_python       | 221 us                                                 | 184 us: 1.20x faster                                                             |
| pyflate                    | 448 ms                                                 | 381 ms: 1.18x faster                                                             |
| chaos                      | 62.8 ms                                                | 53.7 ms: 1.17x faster                                                            |
| tomli_loads                | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.05 sec: 1.17x faster                                                           |
| xml_etree_iterparse        | 96.7 ms                                                | 83.7 ms: 1.16x faster                                                            |
| logging_simple             | 6.63 us                                                | 5.77 us: 1.15x faster                                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                            |
| crypto_pyaes               | 76.6 ms                                                | 67.0 ms: 1.14x faster                                                            |
| logging_format             | 7.35 us                                                | 6.45 us: 1.14x faster                                                            |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.14x faster                                                            |
| regex_compile              | 142 ms                                                 | 127 ms: 1.13x faster                                                             |
| raytrace                   | 299 ms                                                 | 269 ms: 1.11x faster                                                             |
| scimark_lu                 | 114 ms                                                 | 103 ms: 1.10x faster                                                             |
| json_dumps                 | 10.4 ms                                                | 9.48 ms: 1.09x faster                                                            |
| dulwich_log                | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                             |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                            |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                             |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.07x faster                                                           |
| xml_etree_process          | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                            |
| xml_etree_generate         | 85.2 ms                                                | 81.0 ms: 1.05x faster                                                            |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                             |
| pickle_pure_python         | 308 us                                                 | 296 us: 1.04x faster                                                             |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                             |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.27 ms: 1.03x faster                                                            |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                             |
| thrift                     | 791 us                                                 | 771 us: 1.03x faster                                                             |
| fannkuch                   | 372 ms                                                 | 363 ms: 1.03x faster                                                             |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                           |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                             |
| mako                       | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                            |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                            |
| regex_dna                  | 168 ms                                                 | 168 ms: 1.00x slower                                                             |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                            |
| python_startup_no_site     | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                            |
| sympy_sum                  | 166 ms                                                 | 169 ms: 1.02x slower                                                             |
| hexiom                     | 6.17 ms                                                | 6.38 ms: 1.03x slower                                                            |
| sympy_str                  | 292 ms                                                 | 307 ms: 1.05x slower                                                             |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                             |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                             |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                            |
| html5lib                   | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                            |
| genshi_xml                 | 50.2 ms                                                | 54.0 ms: 1.08x slower                                                            |
| sympy_expand               | 468 ms                                                 | 504 ms: 1.08x slower                                                             |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                            |
| nqueens                    | 80.1 ms                                                | 87.6 ms: 1.09x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                                            |
| coverage                   | 71.4 ms                                                | 82.8 ms: 1.16x slower                                                            |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                            |
| gc_traversal               | 3.46 ms                                                | 4.35 ms: 1.26x slower                                                            |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.80x slower                                                            |
| telco                      | 6.53 ms                                                | 160 ms: 24.54x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                                     |

Benchmark hidden because not significant (2): sqlite_synth, django_template
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (9) of results/bm-20251028-3.15.0a1+-7be738d-JIT/bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d.json: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x