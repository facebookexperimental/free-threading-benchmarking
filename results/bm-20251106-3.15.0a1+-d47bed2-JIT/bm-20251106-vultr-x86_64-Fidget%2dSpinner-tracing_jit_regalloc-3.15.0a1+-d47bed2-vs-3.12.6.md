# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: d47bed2
- commit date: 2025-11-06
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                             |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 562 ms: 1.93x faster                                                             |
| async_tree_none            | 464 ms                                                 | 249 ms: 1.87x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 595 ms: 1.86x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                             |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                             |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                                     |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.6 ms: 1.33x faster                                                            |
| nbody          | 89.3 ms                                                | 73.1 ms: 1.22x faster                                                            |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                             |
| regex_effbot   | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                            |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                             |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                             |
| tomli_loads          | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                           |
| xml_etree_iterparse  | 96.7 ms                                                | 84.0 ms: 1.15x faster                                                            |
| json_dumps           | 10.4 ms                                                | 9.11 ms: 1.14x faster                                                            |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                             |
| xml_etree_process    | 59.0 ms                                                | 55.5 ms: 1.06x faster                                                            |
| xml_etree_generate   | 85.2 ms                                                | 80.9 ms: 1.05x faster                                                            |
| pickle_pure_python   | 308 us                                                 | 298 us: 1.03x faster                                                             |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                            |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                            |
| mako            | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                            |
| django_template | 34.7 ms                                                | 35.5 ms: 1.03x slower                                                            |
| genshi_xml      | 50.2 ms                                                | 56.0 ms: 1.12x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.6 ms: 2.23x faster                                                            |
| richards_super             | 51.9 ms                                                | 24.2 ms: 2.14x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 562 ms: 1.93x faster                                                             |
| async_tree_none            | 464 ms                                                 | 249 ms: 1.87x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 595 ms: 1.86x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                             |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.80x faster                                                           |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                             |
| deepcopy_memo              | 40.3 us                                                | 25.5 us: 1.58x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                             |
| go                         | 139 ms                                                 | 101 ms: 1.38x faster                                                             |
| deepcopy                   | 352 us                                                 | 256 us: 1.38x faster                                                             |
| scimark_fft                | 342 ms                                                 | 255 ms: 1.34x faster                                                             |
| float                      | 80.8 ms                                                | 60.6 ms: 1.33x faster                                                            |
| scimark_sor                | 130 ms                                                 | 98.7 ms: 1.31x faster                                                            |
| spectral_norm              | 110 ms                                                 | 86.0 ms: 1.28x faster                                                            |
| logging_silent             | 109 ns                                                 | 85.8 ns: 1.27x faster                                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 55.2 ms: 1.24x faster                                                            |
| nbody                      | 89.3 ms                                                | 73.1 ms: 1.22x faster                                                            |
| deltablue                  | 3.45 ms                                                | 2.84 ms: 1.21x faster                                                            |
| comprehensions             | 19.8 us                                                | 16.4 us: 1.21x faster                                                            |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                            |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                             |
| chaos                      | 62.8 ms                                                | 52.9 ms: 1.19x faster                                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.19x faster                                                            |
| pyflate                    | 448 ms                                                 | 380 ms: 1.18x faster                                                             |
| tomli_loads                | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                           |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.11 sec: 1.15x faster                                                           |
| xml_etree_iterparse        | 96.7 ms                                                | 84.0 ms: 1.15x faster                                                            |
| json_dumps                 | 10.4 ms                                                | 9.11 ms: 1.14x faster                                                            |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                             |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                            |
| logging_format             | 7.35 us                                                | 6.55 us: 1.12x faster                                                            |
| raytrace                   | 299 ms                                                 | 272 ms: 1.10x faster                                                             |
| scimark_lu                 | 114 ms                                                 | 104 ms: 1.09x faster                                                             |
| pprint_safe_repr           | 743 ms                                                 | 686 ms: 1.08x faster                                                             |
| generators                 | 32.2 ms                                                | 29.9 ms: 1.08x faster                                                            |
| regex_effbot               | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                             |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                           |
| xml_etree_process          | 59.0 ms                                                | 55.5 ms: 1.06x faster                                                            |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                            |
| xml_etree_generate         | 85.2 ms                                                | 80.9 ms: 1.05x faster                                                            |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                             |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.21 ms: 1.04x faster                                                            |
| dulwich_log                | 78.9 ms                                                | 76.2 ms: 1.03x faster                                                            |
| pickle_pure_python         | 308 us                                                 | 298 us: 1.03x faster                                                             |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                             |
| fannkuch                   | 372 ms                                                 | 364 ms: 1.02x faster                                                             |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                             |
| mako                       | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                            |
| sympy_integrate            | 20.5 ms                                                | 20.4 ms: 1.01x faster                                                            |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                            |
| sympy_sum                  | 166 ms                                                 | 168 ms: 1.01x slower                                                             |
| python_startup_no_site     | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                            |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.03x slower                                                            |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                             |
| sympy_str                  | 292 ms                                                 | 305 ms: 1.05x slower                                                             |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                             |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                            |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                             |
| sympy_expand               | 468 ms                                                 | 502 ms: 1.07x slower                                                             |
| nqueens                    | 80.1 ms                                                | 86.7 ms: 1.08x slower                                                            |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                            |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                            |
| genshi_xml                 | 50.2 ms                                                | 56.0 ms: 1.12x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 12.6 ms: 1.16x slower                                                            |
| coverage                   | 71.4 ms                                                | 86.0 ms: 1.20x slower                                                            |
| gc_traversal               | 3.46 ms                                                | 4.31 ms: 1.25x slower                                                            |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                            |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                            |
| telco                      | 6.53 ms                                                | 162 ms: 24.74x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                                     |

Benchmark hidden because not significant (5): pylint, thrift, json, coroutines, hexiom
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251106-3.15.0a1+-d47bed2-JIT/bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x