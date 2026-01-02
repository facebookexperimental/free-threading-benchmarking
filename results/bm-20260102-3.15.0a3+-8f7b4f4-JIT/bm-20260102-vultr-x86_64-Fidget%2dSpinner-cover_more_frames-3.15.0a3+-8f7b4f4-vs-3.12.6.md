# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: linux-x86_64
- commit hash: 8f7b4f4
- commit date: 2026-01-02
- overall geometric mean: 1.122x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                          |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.01x slower                                                        |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 545 ms: 1.99x faster                                                          |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                          |
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                                          |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.88x faster                                                          |
| async_tree_memoization     | 555 ms                                                 | 296 ms: 1.88x faster                                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 481 ms: 1.49x faster                                                          |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                          |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                                  |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 57.4 ms: 1.41x faster                                                         |
| nbody          | 89.3 ms                                                | 74.4 ms: 1.20x faster                                                         |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                          |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 121 ms: 1.18x faster                                                          |
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                         |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                          |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                         |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 175 us: 1.26x faster                                                          |
| xml_etree_iterparse  | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                         |
| pickle_pure_python   | 308 us                                                 | 277 us: 1.11x faster                                                          |
| xml_etree_generate   | 85.2 ms                                                | 77.0 ms: 1.11x faster                                                         |
| xml_etree_process    | 59.0 ms                                                | 53.9 ms: 1.09x faster                                                         |
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                        |
| json_dumps           | 10.4 ms                                                | 9.51 ms: 1.09x faster                                                         |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                          |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.38 ms: 1.03x slower                                                         |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                         |
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                         |
| django_template | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                  |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 17.9 ms: 2.56x faster                                                         |
| richards_super             | 51.9 ms                                                | 21.6 ms: 2.41x faster                                                         |
| async_tree_io              | 1.08 sec                                               | 545 ms: 1.99x faster                                                          |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                          |
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                                          |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.88x faster                                                          |
| async_tree_memoization     | 555 ms                                                 | 296 ms: 1.88x faster                                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                          |
| mdp                        | 2.42 sec                                               | 1.35 sec: 1.79x faster                                                        |
| deepcopy_memo              | 40.3 us                                                | 24.9 us: 1.62x faster                                                         |
| go                         | 139 ms                                                 | 91.8 ms: 1.52x faster                                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 481 ms: 1.49x faster                                                          |
| deepcopy                   | 352 us                                                 | 240 us: 1.47x faster                                                          |
| float                      | 80.8 ms                                                | 57.4 ms: 1.41x faster                                                         |
| scimark_fft                | 342 ms                                                 | 259 ms: 1.32x faster                                                          |
| scimark_monte_carlo        | 68.4 ms                                                | 52.1 ms: 1.31x faster                                                         |
| logging_silent             | 109 ns                                                 | 83.3 ns: 1.31x faster                                                         |
| deltablue                  | 3.45 ms                                                | 2.65 ms: 1.30x faster                                                         |
| spectral_norm              | 110 ms                                                 | 86.9 ms: 1.27x faster                                                         |
| scimark_sor                | 130 ms                                                 | 103 ms: 1.26x faster                                                          |
| unpickle_pure_python       | 221 us                                                 | 175 us: 1.26x faster                                                          |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                         |
| pyflate                    | 448 ms                                                 | 365 ms: 1.23x faster                                                          |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                         |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                         |
| chaos                      | 62.8 ms                                                | 51.9 ms: 1.21x faster                                                         |
| nbody                      | 89.3 ms                                                | 74.4 ms: 1.20x faster                                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.01 sec: 1.18x faster                                                        |
| regex_compile              | 142 ms                                                 | 121 ms: 1.18x faster                                                          |
| pprint_pformat             | 1.52 sec                                               | 1.30 sec: 1.17x faster                                                        |
| crypto_pyaes               | 76.6 ms                                                | 65.9 ms: 1.16x faster                                                         |
| pprint_safe_repr           | 743 ms                                                 | 640 ms: 1.16x faster                                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                         |
| scimark_lu                 | 114 ms                                                 | 98.8 ms: 1.16x faster                                                         |
| logging_simple             | 6.63 us                                                | 5.77 us: 1.15x faster                                                         |
| raytrace                   | 299 ms                                                 | 261 ms: 1.15x faster                                                          |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                         |
| logging_format             | 7.35 us                                                | 6.48 us: 1.13x faster                                                         |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                         |
| pickle_pure_python         | 308 us                                                 | 277 us: 1.11x faster                                                          |
| xml_etree_generate         | 85.2 ms                                                | 77.0 ms: 1.11x faster                                                         |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                         |
| dulwich_log                | 78.9 ms                                                | 71.8 ms: 1.10x faster                                                         |
| thrift                     | 791 us                                                 | 723 us: 1.10x faster                                                          |
| xml_etree_process          | 59.0 ms                                                | 53.9 ms: 1.09x faster                                                         |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                        |
| json_dumps                 | 10.4 ms                                                | 9.51 ms: 1.09x faster                                                         |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                          |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.08x faster                                                        |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                          |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.06x faster                                                          |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                          |
| meteor_contest             | 104 ms                                                 | 98.3 ms: 1.05x faster                                                         |
| fannkuch                   | 372 ms                                                 | 354 ms: 1.05x faster                                                          |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                         |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                          |
| hexiom                     | 6.17 ms                                                | 6.03 ms: 1.02x faster                                                         |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                         |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.01x slower                                                        |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.46 ms: 1.01x slower                                                         |
| django_template            | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                         |
| sympy_sum                  | 166 ms                                                 | 170 ms: 1.02x slower                                                          |
| python_startup_no_site     | 7.16 ms                                                | 7.38 ms: 1.03x slower                                                         |
| nqueens                    | 80.1 ms                                                | 83.7 ms: 1.05x slower                                                         |
| sympy_str                  | 292 ms                                                 | 306 ms: 1.05x slower                                                          |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                          |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                         |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                          |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                          |
| sympy_expand               | 468 ms                                                 | 519 ms: 1.11x slower                                                          |
| coverage                   | 71.4 ms                                                | 81.8 ms: 1.15x slower                                                         |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                         |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                         |
| gc_traversal               | 3.46 ms                                                | 4.47 ms: 1.29x slower                                                         |
| bench_thread_pool          | 941 us                                                 | 1.30 ms: 1.38x slower                                                         |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                         |
| bench_mp_pool              | 10.8 ms                                                | 220 ms: 20.36x slower                                                         |
| telco                      | 6.53 ms                                                | 160 ms: 24.59x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                                  |

Benchmark hidden because not significant (5): json, sqlite_synth, coroutines, html5lib, genshi_xml
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260102-3.15.0a3+-8f7b4f4-JIT/bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.122x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x