# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 5d987e8
- commit date: 2026-01-10
- overall geometric mean: 1.019x slower
- HPT reliability: 67.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 278 ms: 1.07x slower                                               |
| docutils       | 2.62 sec                                                     | 2.90 sec: 1.11x slower                                             |
| html5lib       | 67.0 ms                                                      | 69.9 ms: 1.04x slower                                              |
| Geometric mean | (ref)                                                        | 1.07x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 598 ms: 1.53x faster                                               |
| async_tree_io              | 876 ms                                                       | 620 ms: 1.41x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.27x faster                                               |
| async_tree_none            | 354 ms                                                       | 280 ms: 1.26x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 548 ms: 1.22x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 528 ms: 1.21x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                               |
| async_generators           | 377 ms                                                       | 394 ms: 1.04x slower                                               |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                       |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 55.4 ms: 1.40x faster                                              |
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                               |
| nbody          | 85.1 ms                                                      | 91.9 ms: 1.08x slower                                              |
| Geometric mean | (ref)                                                        | 1.14x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                              |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                              |
| regex_dna      | 180 ms                                                       | 174 ms: 1.03x faster                                               |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                              |
| tomli_loads          | 2.01 sec                                                     | 1.87 sec: 1.07x faster                                             |
| unpickle_pure_python | 210 us                                                       | 200 us: 1.05x faster                                               |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                               |
| xml_etree_generate   | 85.4 ms                                                      | 89.7 ms: 1.05x slower                                              |
| pickle_pure_python   | 294 us                                                       | 311 us: 1.06x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 63.7 ms: 1.07x slower                                              |
| json_loads           | 27.0 us                                                      | 32.2 us: 1.19x slower                                              |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                       |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                              |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                              |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 42.2 ms: 1.24x slower                                              |
| mako            | 11.3 ms                                                      | 14.5 ms: 1.28x slower                                              |
| genshi_text     | 21.5 ms                                                      | 28.3 ms: 1.31x slower                                              |
| genshi_xml      | 48.8 ms                                                      | 68.2 ms: 1.40x slower                                              |
| Geometric mean  | (ref)                                                        | 1.31x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.1 ms: 2.25x faster                                              |
| richards_super             | 51.6 ms                                                      | 25.1 ms: 2.06x faster                                              |
| gc_traversal               | 3.14 ms                                                      | 1.90 ms: 1.66x faster                                              |
| bench_mp_pool              | 11.0 ms                                                      | 7.02 ms: 1.57x faster                                              |
| async_tree_io_tg           | 913 ms                                                       | 598 ms: 1.53x faster                                               |
| mdp                        | 2.36 sec                                                     | 1.57 sec: 1.50x faster                                             |
| async_tree_io              | 876 ms                                                       | 620 ms: 1.41x faster                                               |
| deepcopy_memo              | 39.1 us                                                      | 27.9 us: 1.40x faster                                              |
| float                      | 77.5 ms                                                      | 55.4 ms: 1.40x faster                                              |
| deepcopy                   | 355 us                                                       | 261 us: 1.36x faster                                               |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.27x faster                                               |
| async_tree_none            | 354 ms                                                       | 280 ms: 1.26x faster                                               |
| logging_silent             | 103 ns                                                       | 83.0 ns: 1.24x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 548 ms: 1.22x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 528 ms: 1.21x faster                                               |
| scimark_fft                | 349 ms                                                       | 293 ms: 1.19x faster                                               |
| pyflate                    | 449 ms                                                       | 385 ms: 1.16x faster                                               |
| scimark_sor                | 134 ms                                                       | 116 ms: 1.16x faster                                               |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                               |
| spectral_norm              | 111 ms                                                       | 98.8 ms: 1.12x faster                                              |
| deepcopy_reduce            | 3.11 us                                                      | 2.78 us: 1.12x faster                                              |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                              |
| sqlite_synth               | 2.21 us                                                      | 2.02 us: 1.09x faster                                              |
| bpe_tokeniser              | 4.45 sec                                                     | 4.07 sec: 1.09x faster                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                              |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                              |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                              |
| tomli_loads                | 2.01 sec                                                     | 1.87 sec: 1.07x faster                                             |
| pprint_safe_repr           | 738 ms                                                       | 700 ms: 1.05x faster                                               |
| unpickle_pure_python       | 210 us                                                       | 200 us: 1.05x faster                                               |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                               |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.03x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                               |
| deltablue                  | 3.12 ms                                                      | 3.07 ms: 1.02x faster                                              |
| scimark_monte_carlo        | 65.4 ms                                                      | 66.5 ms: 1.02x slower                                              |
| chaos                      | 57.3 ms                                                      | 59.4 ms: 1.04x slower                                              |
| html5lib                   | 67.0 ms                                                      | 69.9 ms: 1.04x slower                                              |
| async_generators           | 377 ms                                                       | 394 ms: 1.04x slower                                               |
| scimark_lu                 | 113 ms                                                       | 118 ms: 1.05x slower                                               |
| xml_etree_generate         | 85.4 ms                                                      | 89.7 ms: 1.05x slower                                              |
| pickle_pure_python         | 294 us                                                       | 311 us: 1.06x slower                                               |
| 2to3                       | 260 ms                                                       | 278 ms: 1.07x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 63.7 ms: 1.07x slower                                              |
| nbody                      | 85.1 ms                                                      | 91.9 ms: 1.08x slower                                              |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                               |
| json                       | 4.93 ms                                                      | 5.35 ms: 1.08x slower                                              |
| create_gc_cycles           | 1.34 ms                                                      | 1.47 ms: 1.10x slower                                              |
| comprehensions             | 16.5 us                                                      | 18.1 us: 1.10x slower                                              |
| fannkuch                   | 370 ms                                                       | 408 ms: 1.10x slower                                               |
| docutils                   | 2.62 sec                                                     | 2.90 sec: 1.11x slower                                             |
| thrift                     | 778 us                                                       | 881 us: 1.13x slower                                               |
| logging_simple             | 6.16 us                                                      | 7.01 us: 1.14x slower                                              |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.38 ms: 1.14x slower                                              |
| logging_format             | 6.84 us                                                      | 7.82 us: 1.14x slower                                              |
| sympy_integrate            | 19.8 ms                                                      | 23.0 ms: 1.16x slower                                              |
| hexiom                     | 5.99 ms                                                      | 6.96 ms: 1.16x slower                                              |
| generators                 | 28.8 ms                                                      | 33.7 ms: 1.17x slower                                              |
| nqueens                    | 78.6 ms                                                      | 92.0 ms: 1.17x slower                                              |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                               |
| json_loads                 | 27.0 us                                                      | 32.2 us: 1.19x slower                                              |
| raytrace                   | 253 ms                                                       | 307 ms: 1.21x slower                                               |
| crypto_pyaes               | 67.9 ms                                                      | 82.5 ms: 1.21x slower                                              |
| django_template            | 34.1 ms                                                      | 42.2 ms: 1.24x slower                                              |
| sympy_sum                  | 156 ms                                                       | 193 ms: 1.24x slower                                               |
| typing_runtime_protocols   | 155 us                                                       | 195 us: 1.26x slower                                               |
| sympy_expand               | 457 ms                                                       | 578 ms: 1.27x slower                                               |
| mako                       | 11.3 ms                                                      | 14.5 ms: 1.28x slower                                              |
| python_startup_no_site     | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                              |
| sympy_str                  | 275 ms                                                       | 356 ms: 1.30x slower                                               |
| genshi_text                | 21.5 ms                                                      | 28.3 ms: 1.31x slower                                              |
| coverage                   | 83.0 ms                                                      | 112 ms: 1.35x slower                                               |
| genshi_xml                 | 48.8 ms                                                      | 68.2 ms: 1.40x slower                                              |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                              |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                              |
| telco                      | 7.82 ms                                                      | 180 ms: 23.06x slower                                              |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                       |

Benchmark hidden because not significant (6): pprint_pformat, dulwich_log, json_dumps, coroutines, pycparser, pylint
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-5d987e8-JIT,NOGIL/bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 67.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.43x