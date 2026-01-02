# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: linux-x86_64
- commit hash: b1e4adf
- commit date: 2026-01-01
- overall geometric mean: 1.130x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                          |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.01x slower                                                        |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 548 ms: 1.98x faster                                                          |
| async_tree_none            | 464 ms                                                 | 237 ms: 1.96x faster                                                          |
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                          |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                          |
| async_tree_memoization     | 555 ms                                                 | 298 ms: 1.86x faster                                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 476 ms: 1.50x faster                                                          |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                          |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                         |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 57.5 ms: 1.40x faster                                                         |
| nbody          | 89.3 ms                                                | 73.9 ms: 1.21x faster                                                         |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                  | 1.17x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 120 ms: 1.18x faster                                                          |
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                         |
| regex_dna      | 168 ms                                                 | 167 ms: 1.01x faster                                                          |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 177 us: 1.24x faster                                                          |
| xml_etree_iterparse  | 96.7 ms                                                | 83.7 ms: 1.16x faster                                                         |
| pickle_pure_python   | 308 us                                                 | 275 us: 1.12x faster                                                          |
| json_dumps           | 10.4 ms                                                | 9.36 ms: 1.11x faster                                                         |
| xml_etree_generate   | 85.2 ms                                                | 77.4 ms: 1.10x faster                                                         |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                          |
| xml_etree_process    | 59.0 ms                                                | 54.8 ms: 1.08x faster                                                         |
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                        |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                         |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                         |
| mako            | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                         |
| genshi_xml      | 50.2 ms                                                | 49.3 ms: 1.02x faster                                                         |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 17.9 ms: 2.57x faster                                                         |
| richards_super             | 51.9 ms                                                | 21.3 ms: 2.44x faster                                                         |
| async_tree_io              | 1.08 sec                                               | 548 ms: 1.98x faster                                                          |
| async_tree_none            | 464 ms                                                 | 237 ms: 1.96x faster                                                          |
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                          |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                          |
| async_tree_memoization     | 555 ms                                                 | 298 ms: 1.86x faster                                                          |
| mdp                        | 2.42 sec                                               | 1.35 sec: 1.80x faster                                                        |
| deepcopy_memo              | 40.3 us                                                | 24.8 us: 1.62x faster                                                         |
| go                         | 139 ms                                                 | 91.4 ms: 1.52x faster                                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 476 ms: 1.50x faster                                                          |
| deepcopy                   | 352 us                                                 | 238 us: 1.48x faster                                                          |
| float                      | 80.8 ms                                                | 57.5 ms: 1.40x faster                                                         |
| scimark_fft                | 342 ms                                                 | 260 ms: 1.31x faster                                                          |
| deltablue                  | 3.45 ms                                                | 2.64 ms: 1.31x faster                                                         |
| scimark_monte_carlo        | 68.4 ms                                                | 52.4 ms: 1.31x faster                                                         |
| logging_silent             | 109 ns                                                 | 83.8 ns: 1.30x faster                                                         |
| spectral_norm              | 110 ms                                                 | 85.8 ms: 1.28x faster                                                         |
| scimark_sor                | 130 ms                                                 | 101 ms: 1.28x faster                                                          |
| pyflate                    | 448 ms                                                 | 357 ms: 1.26x faster                                                          |
| unpickle_pure_python       | 221 us                                                 | 177 us: 1.24x faster                                                          |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                         |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                         |
| nbody                      | 89.3 ms                                                | 73.9 ms: 1.21x faster                                                         |
| deepcopy_reduce            | 3.08 us                                                | 2.56 us: 1.20x faster                                                         |
| regex_compile              | 142 ms                                                 | 120 ms: 1.18x faster                                                          |
| pprint_safe_repr           | 743 ms                                                 | 628 ms: 1.18x faster                                                          |
| pprint_pformat             | 1.52 sec                                               | 1.29 sec: 1.18x faster                                                        |
| chaos                      | 62.8 ms                                                | 53.4 ms: 1.18x faster                                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                        |
| scimark_lu                 | 114 ms                                                 | 98.1 ms: 1.16x faster                                                         |
| crypto_pyaes               | 76.6 ms                                                | 66.0 ms: 1.16x faster                                                         |
| xml_etree_iterparse        | 96.7 ms                                                | 83.7 ms: 1.16x faster                                                         |
| raytrace                   | 299 ms                                                 | 261 ms: 1.15x faster                                                          |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                         |
| logging_simple             | 6.63 us                                                | 5.86 us: 1.13x faster                                                         |
| genshi_text                | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                         |
| pickle_pure_python         | 308 us                                                 | 275 us: 1.12x faster                                                          |
| logging_format             | 7.35 us                                                | 6.58 us: 1.12x faster                                                         |
| dulwich_log                | 78.9 ms                                                | 70.7 ms: 1.12x faster                                                         |
| json_dumps                 | 10.4 ms                                                | 9.36 ms: 1.11x faster                                                         |
| generators                 | 32.2 ms                                                | 29.3 ms: 1.10x faster                                                         |
| xml_etree_generate         | 85.2 ms                                                | 77.4 ms: 1.10x faster                                                         |
| thrift                     | 791 us                                                 | 727 us: 1.09x faster                                                          |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                          |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.08x faster                                                        |
| xml_etree_process          | 59.0 ms                                                | 54.8 ms: 1.08x faster                                                         |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                          |
| fannkuch                   | 372 ms                                                 | 349 ms: 1.07x faster                                                          |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                        |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                          |
| meteor_contest             | 104 ms                                                 | 98.3 ms: 1.05x faster                                                         |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.04x faster                                                          |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                          |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                         |
| hexiom                     | 6.17 ms                                                | 6.00 ms: 1.03x faster                                                         |
| sympy_integrate            | 20.5 ms                                                | 20.1 ms: 1.02x faster                                                         |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                         |
| genshi_xml                 | 50.2 ms                                                | 49.3 ms: 1.02x faster                                                         |
| regex_dna                  | 168 ms                                                 | 167 ms: 1.01x faster                                                          |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                         |
| sympy_sum                  | 166 ms                                                 | 167 ms: 1.01x slower                                                          |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                         |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.01x slower                                                        |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                         |
| sympy_str                  | 292 ms                                                 | 302 ms: 1.04x slower                                                          |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                          |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                         |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                          |
| nqueens                    | 80.1 ms                                                | 84.4 ms: 1.05x slower                                                         |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                         |
| sympy_expand               | 468 ms                                                 | 508 ms: 1.09x slower                                                          |
| coverage                   | 71.4 ms                                                | 80.7 ms: 1.13x slower                                                         |
| gc_traversal               | 3.46 ms                                                | 4.04 ms: 1.17x slower                                                         |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                         |
| bench_thread_pool          | 941 us                                                 | 1.30 ms: 1.38x slower                                                         |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                         |
| bench_mp_pool              | 10.8 ms                                                | 258 ms: 23.88x slower                                                         |
| telco                      | 6.53 ms                                                | 159 ms: 24.42x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                                  |

Benchmark hidden because not significant (2): sqlite_synth, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260101-3.15.0a3+-b1e4adf-JIT/bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.130x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x