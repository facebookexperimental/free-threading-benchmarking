# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: d47bed2
- commit date: 2025-11-06
- overall geometric mean: 1.062x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.03x faster                                                             |
| html5lib       | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 562 ms: 1.56x faster                                                             |
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.53x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                             |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                             |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                             |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.6 ms: 1.28x faster                                                            |
| nbody          | 85.1 ms                                                      | 73.1 ms: 1.16x faster                                                            |
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                             |
| Geometric mean | (ref)                                                        | 1.19x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                             |
| regex_effbot   | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                            |
| regex_dna      | 180 ms                                                       | 180 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                        | 1.03x faster                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.11 ms: 1.16x faster                                                            |
| unpickle_pure_python | 210 us                                                       | 185 us: 1.14x faster                                                             |
| xml_etree_iterparse  | 94.9 ms                                                      | 84.0 ms: 1.13x faster                                                            |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                           |
| xml_etree_process    | 59.3 ms                                                      | 55.5 ms: 1.07x faster                                                            |
| xml_etree_generate   | 85.4 ms                                                      | 80.9 ms: 1.06x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                             |
| pickle_pure_python   | 294 us                                                       | 298 us: 1.01x slower                                                             |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.26 ms: 1.02x faster                                                            |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                            |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                            |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                            |
| genshi_xml      | 48.8 ms                                                      | 56.0 ms: 1.15x slower                                                            |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.6 ms: 2.19x faster                                                            |
| richards_super             | 51.6 ms                                                      | 24.2 ms: 2.13x faster                                                            |
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                                           |
| async_tree_io              | 876 ms                                                       | 562 ms: 1.56x faster                                                             |
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.53x faster                                                             |
| deepcopy_memo              | 39.1 us                                                      | 25.5 us: 1.53x faster                                                            |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                             |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                             |
| go                         | 141 ms                                                       | 101 ms: 1.39x faster                                                             |
| deepcopy                   | 355 us                                                       | 256 us: 1.39x faster                                                             |
| scimark_fft                | 349 ms                                                       | 255 ms: 1.37x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                             |
| scimark_sor                | 134 ms                                                       | 98.7 ms: 1.36x faster                                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                             |
| spectral_norm              | 111 ms                                                       | 86.0 ms: 1.29x faster                                                            |
| float                      | 77.5 ms                                                      | 60.6 ms: 1.28x faster                                                            |
| deepcopy_reduce            | 3.11 us                                                      | 2.60 us: 1.20x faster                                                            |
| logging_silent             | 103 ns                                                       | 85.8 ns: 1.19x faster                                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.2 ms: 1.18x faster                                                            |
| pyflate                    | 449 ms                                                       | 380 ms: 1.18x faster                                                             |
| nbody                      | 85.1 ms                                                      | 73.1 ms: 1.16x faster                                                            |
| json_dumps                 | 10.5 ms                                                      | 9.11 ms: 1.16x faster                                                            |
| unpickle_pure_python       | 210 us                                                       | 185 us: 1.14x faster                                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.0 ms: 1.13x faster                                                            |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                             |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.21 ms: 1.12x faster                                                            |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                           |
| deltablue                  | 3.12 ms                                                      | 2.84 ms: 1.10x faster                                                            |
| chaos                      | 57.3 ms                                                      | 52.9 ms: 1.08x faster                                                            |
| bpe_tokeniser              | 4.45 sec                                                     | 4.11 sec: 1.08x faster                                                           |
| scimark_lu                 | 113 ms                                                       | 104 ms: 1.08x faster                                                             |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                            |
| pprint_safe_repr           | 738 ms                                                       | 686 ms: 1.07x faster                                                             |
| xml_etree_process          | 59.3 ms                                                      | 55.5 ms: 1.07x faster                                                            |
| xml_etree_generate         | 85.4 ms                                                      | 80.9 ms: 1.06x faster                                                            |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                             |
| mako                       | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                            |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.05x faster                                                           |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                             |
| regex_effbot               | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                            |
| logging_simple             | 6.16 us                                                      | 5.88 us: 1.05x faster                                                            |
| logging_format             | 6.84 us                                                      | 6.55 us: 1.04x faster                                                            |
| 2to3                       | 260 ms                                                       | 251 ms: 1.03x faster                                                             |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                             |
| crypto_pyaes               | 67.9 ms                                                      | 66.3 ms: 1.02x faster                                                            |
| python_startup_no_site     | 7.39 ms                                                      | 7.26 ms: 1.02x faster                                                            |
| fannkuch                   | 370 ms                                                       | 364 ms: 1.02x faster                                                             |
| regex_dna                  | 180 ms                                                       | 180 ms: 1.00x faster                                                             |
| comprehensions             | 16.5 us                                                      | 16.4 us: 1.00x faster                                                            |
| thrift                     | 778 us                                                       | 785 us: 1.01x slower                                                             |
| pickle_pure_python         | 294 us                                                       | 298 us: 1.01x slower                                                             |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                            |
| json                       | 4.93 ms                                                      | 5.00 ms: 1.02x slower                                                            |
| dulwich_log                | 74.8 ms                                                      | 76.2 ms: 1.02x slower                                                            |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                             |
| sympy_integrate            | 19.8 ms                                                      | 20.4 ms: 1.03x slower                                                            |
| hexiom                     | 5.99 ms                                                      | 6.17 ms: 1.03x slower                                                            |
| coverage                   | 83.0 ms                                                      | 86.0 ms: 1.04x slower                                                            |
| generators                 | 28.8 ms                                                      | 29.9 ms: 1.04x slower                                                            |
| html5lib                   | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                            |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                            |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                             |
| raytrace                   | 253 ms                                                       | 272 ms: 1.08x slower                                                             |
| sympy_sum                  | 156 ms                                                       | 168 ms: 1.08x slower                                                             |
| sympy_expand               | 457 ms                                                       | 502 ms: 1.10x slower                                                             |
| nqueens                    | 78.6 ms                                                      | 86.7 ms: 1.10x slower                                                            |
| sympy_str                  | 275 ms                                                       | 305 ms: 1.11x slower                                                             |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                            |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                            |
| genshi_xml                 | 48.8 ms                                                      | 56.0 ms: 1.15x slower                                                            |
| gc_traversal               | 3.14 ms                                                      | 4.31 ms: 1.37x slower                                                            |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                            |
| telco                      | 7.82 ms                                                      | 162 ms: 20.64x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                     |

Benchmark hidden because not significant (5): pylint, meteor_contest, genshi_text, regex_v8, sqlite_synth
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, pycparser, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251106-3.15.0a1+-d47bed2-JIT/bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x