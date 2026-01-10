# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 5d987e8
- commit date: 2026-01-10
- overall geometric mean: 1.015x faster
- HPT reliability: 81.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.06x slower                                               |
| docutils       | 2.64 sec                                               | 2.90 sec: 1.10x slower                                             |
| html5lib       | 63.6 ms                                                | 69.9 ms: 1.10x slower                                              |
| Geometric mean | (ref)                                                  | 1.08x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 598 ms: 1.85x faster                                               |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                               |
| async_tree_none            | 464 ms                                                 | 280 ms: 1.66x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 528 ms: 1.37x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                               |
| async_generators           | 384 ms                                                 | 394 ms: 1.03x slower                                               |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 55.4 ms: 1.46x faster                                              |
| nbody          | 89.3 ms                                                | 91.9 ms: 1.03x slower                                              |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                  | 1.11x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                              |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                               |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                  | 1.02x faster                                                       |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.87 sec: 1.12x faster                                             |
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                              |
| unpickle_pure_python | 221 us                                                 | 200 us: 1.10x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.05x faster                                               |
| pickle_pure_python   | 308 us                                                 | 311 us: 1.01x slower                                               |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.02x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 89.7 ms: 1.05x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 63.7 ms: 1.08x slower                                              |
| json_loads           | 26.5 us                                                | 32.2 us: 1.21x slower                                              |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                              |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                              |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.2 ms: 1.22x slower                                              |
| genshi_text     | 22.8 ms                                                | 28.3 ms: 1.24x slower                                              |
| mako            | 11.0 ms                                                | 14.5 ms: 1.32x slower                                              |
| genshi_xml      | 50.2 ms                                                | 68.2 ms: 1.36x slower                                              |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.1 ms: 2.28x faster                                              |
| richards_super             | 51.9 ms                                                | 25.1 ms: 2.07x faster                                              |
| async_tree_io_tg           | 1.11 sec                                               | 598 ms: 1.85x faster                                               |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.82x faster                                              |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                               |
| async_tree_none            | 464 ms                                                 | 280 ms: 1.66x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                               |
| mdp                        | 2.42 sec                                               | 1.57 sec: 1.54x faster                                             |
| bench_mp_pool              | 10.8 ms                                                | 7.02 ms: 1.54x faster                                              |
| float                      | 80.8 ms                                                | 55.4 ms: 1.46x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 27.9 us: 1.44x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 528 ms: 1.37x faster                                               |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                               |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                               |
| logging_silent             | 109 ns                                                 | 83.0 ns: 1.31x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                               |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                              |
| scimark_fft                | 342 ms                                                 | 293 ms: 1.17x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.07 sec: 1.16x faster                                             |
| pyflate                    | 448 ms                                                 | 385 ms: 1.16x faster                                               |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                              |
| tomli_loads                | 2.11 sec                                               | 1.87 sec: 1.12x faster                                             |
| deltablue                  | 3.45 ms                                                | 3.07 ms: 1.12x faster                                              |
| spectral_norm              | 110 ms                                                 | 98.8 ms: 1.11x faster                                              |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.11x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 2.78 us: 1.11x faster                                              |
| unpickle_pure_python       | 221 us                                                 | 200 us: 1.10x faster                                               |
| comprehensions             | 19.8 us                                                | 18.1 us: 1.09x faster                                              |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                              |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                               |
| chaos                      | 62.8 ms                                                | 59.4 ms: 1.06x faster                                              |
| dulwich_log                | 78.9 ms                                                | 74.6 ms: 1.06x faster                                              |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.05x faster                                               |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 66.5 ms: 1.03x faster                                              |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                               |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                               |
| pickle_pure_python         | 308 us                                                 | 311 us: 1.01x slower                                               |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.02x slower                                              |
| raytrace                   | 299 ms                                                 | 307 ms: 1.02x slower                                               |
| async_generators           | 384 ms                                                 | 394 ms: 1.03x slower                                               |
| nbody                      | 89.3 ms                                                | 91.9 ms: 1.03x slower                                              |
| scimark_lu                 | 114 ms                                                 | 118 ms: 1.03x slower                                               |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                               |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                               |
| generators                 | 32.2 ms                                                | 33.7 ms: 1.05x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 89.7 ms: 1.05x slower                                              |
| 2to3                       | 264 ms                                                 | 278 ms: 1.06x slower                                               |
| logging_simple             | 6.63 us                                                | 7.01 us: 1.06x slower                                              |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                              |
| logging_format             | 7.35 us                                                | 7.82 us: 1.06x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 82.5 ms: 1.08x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 63.7 ms: 1.08x slower                                              |
| fannkuch                   | 372 ms                                                 | 408 ms: 1.10x slower                                               |
| docutils                   | 2.64 sec                                               | 2.90 sec: 1.10x slower                                             |
| html5lib                   | 63.6 ms                                                | 69.9 ms: 1.10x slower                                              |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                               |
| sympy_integrate            | 20.5 ms                                                | 23.0 ms: 1.12x slower                                              |
| hexiom                     | 6.17 ms                                                | 6.96 ms: 1.13x slower                                              |
| nqueens                    | 80.1 ms                                                | 92.0 ms: 1.15x slower                                              |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                               |
| sympy_sum                  | 166 ms                                                 | 193 ms: 1.16x slower                                               |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.20x slower                                               |
| json_loads                 | 26.5 us                                                | 32.2 us: 1.21x slower                                              |
| django_template            | 34.7 ms                                                | 42.2 ms: 1.22x slower                                              |
| sympy_str                  | 292 ms                                                 | 356 ms: 1.22x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.38 ms: 1.22x slower                                              |
| sympy_expand               | 468 ms                                                 | 578 ms: 1.24x slower                                               |
| genshi_text                | 22.8 ms                                                | 28.3 ms: 1.24x slower                                              |
| mako                       | 11.0 ms                                                | 14.5 ms: 1.32x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.47 ms: 1.35x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 68.2 ms: 1.36x slower                                              |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.56x slower                                              |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                               |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                              |
| telco                      | 6.53 ms                                                | 180 ms: 27.64x slower                                              |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                       |

Benchmark hidden because not significant (2): regex_v8, pylint
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-5d987e8-JIT,NOGIL/bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 81.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.44x