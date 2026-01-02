# Results vs. base

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: linux-x86_64
- commit hash: 8f7b4f4
- commit date: 2026-01-02
- overall geometric mean: 1.000x slower
- HPT reliability: 99.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 250 ms: 1.01x slower                                                          |
| docutils       | 2.69 sec                                                               | 2.68 sec: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                  |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization     | 304 ms                                                                 | 296 ms: 1.03x faster                                                          |
| async_tree_none_tg         | 243 ms                                                                 | 237 ms: 1.02x faster                                                          |
| async_tree_memoization_tg  | 306 ms                                                                 | 300 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 480 ms: 1.02x faster                                                          |
| async_tree_io_tg           | 588 ms                                                                 | 578 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed    | 489 ms                                                                 | 481 ms: 1.02x faster                                                          |
| async_generators           | 362 ms                                                                 | 359 ms: 1.01x faster                                                          |
| asyncio_websockets         | 544 ms                                                                 | 543 ms: 1.00x faster                                                          |
| coroutines                 | 23.4 ms                                                                | 24.0 ms: 1.02x slower                                                         |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (2): async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 75.3 ms                                                                | 74.4 ms: 1.01x faster                                                         |
| pidigits       | 192 ms                                                                 | 201 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 2.56 ms                                                                | 2.78 ms: 1.09x slower                                                         |
| regex_dna      | 168 ms                                                                 | 183 ms: 1.09x slower                                                          |
| regex_v8       | 21.2 ms                                                                | 24.0 ms: 1.13x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                                  |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1.98 sec                                                               | 1.93 sec: 1.03x faster                                                        |
| xml_etree_generate   | 78.6 ms                                                                | 77.0 ms: 1.02x faster                                                         |
| xml_etree_process    | 54.7 ms                                                                | 53.9 ms: 1.02x faster                                                         |
| unpickle_pure_python | 178 us                                                                 | 175 us: 1.01x faster                                                          |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                          |
| xml_etree_iterparse  | 84.0 ms                                                                | 83.4 ms: 1.01x faster                                                         |
| json_loads           | 28.1 us                                                                | 28.5 us: 1.01x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (2): pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                                | 7.38 ms: 1.01x slower                                                         |
| python_startup         | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                         |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 52.1 ms                                                                | 50.6 ms: 1.03x faster                                                         |
| genshi_text    | 21.2 ms                                                                | 20.7 ms: 1.03x faster                                                         |
| mako           | 10.4 ms                                                                | 10.5 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| logging_format             | 6.76 us                                                                | 6.48 us: 1.04x faster                                                         |
| nqueens                    | 86.8 ms                                                                | 83.7 ms: 1.04x faster                                                         |
| genshi_xml                 | 52.1 ms                                                                | 50.6 ms: 1.03x faster                                                         |
| pycparser                  | 1.11 sec                                                               | 1.08 sec: 1.03x faster                                                        |
| async_tree_memoization     | 304 ms                                                                 | 296 ms: 1.03x faster                                                          |
| tomli_loads                | 1.98 sec                                                               | 1.93 sec: 1.03x faster                                                        |
| genshi_text                | 21.2 ms                                                                | 20.7 ms: 1.03x faster                                                         |
| chaos                      | 53.2 ms                                                                | 51.9 ms: 1.03x faster                                                         |
| scimark_monte_carlo        | 53.4 ms                                                                | 52.1 ms: 1.02x faster                                                         |
| raytrace                   | 267 ms                                                                 | 261 ms: 1.02x faster                                                          |
| async_tree_none_tg         | 243 ms                                                                 | 237 ms: 1.02x faster                                                          |
| deepcopy_reduce            | 2.60 us                                                                | 2.54 us: 1.02x faster                                                         |
| logging_simple             | 5.90 us                                                                | 5.77 us: 1.02x faster                                                         |
| sqlglot_v2_normalize       | 109 ms                                                                 | 106 ms: 1.02x faster                                                          |
| xml_etree_generate         | 78.6 ms                                                                | 77.0 ms: 1.02x faster                                                         |
| async_tree_memoization_tg  | 306 ms                                                                 | 300 ms: 1.02x faster                                                          |
| deepcopy                   | 244 us                                                                 | 240 us: 1.02x faster                                                          |
| pprint_pformat             | 1.33 sec                                                               | 1.30 sec: 1.02x faster                                                        |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 480 ms: 1.02x faster                                                          |
| async_tree_io_tg           | 588 ms                                                                 | 578 ms: 1.02x faster                                                          |
| crypto_pyaes               | 67.0 ms                                                                | 65.9 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed    | 489 ms                                                                 | 481 ms: 1.02x faster                                                          |
| thrift                     | 734 us                                                                 | 723 us: 1.02x faster                                                          |
| telco                      | 163 ms                                                                 | 160 ms: 1.02x faster                                                          |
| xml_etree_process          | 54.7 ms                                                                | 53.9 ms: 1.02x faster                                                         |
| unpickle_pure_python       | 178 us                                                                 | 175 us: 1.01x faster                                                          |
| connected_components       | 380 ms                                                                 | 376 ms: 1.01x faster                                                          |
| deltablue                  | 2.68 ms                                                                | 2.65 ms: 1.01x faster                                                         |
| nbody                      | 75.3 ms                                                                | 74.4 ms: 1.01x faster                                                         |
| hexiom                     | 6.09 ms                                                                | 6.03 ms: 1.01x faster                                                         |
| pathlib                    | 17.7 ms                                                                | 17.5 ms: 1.01x faster                                                         |
| deepcopy_memo              | 25.1 us                                                                | 24.9 us: 1.01x faster                                                         |
| bench_thread_pool          | 1.31 ms                                                                | 1.30 ms: 1.01x faster                                                         |
| mdp                        | 1.37 sec                                                               | 1.35 sec: 1.01x faster                                                        |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                          |
| async_generators           | 362 ms                                                                 | 359 ms: 1.01x faster                                                          |
| sympy_str                  | 309 ms                                                                 | 306 ms: 1.01x faster                                                          |
| k_core                     | 1.88 sec                                                               | 1.86 sec: 1.01x faster                                                        |
| xml_etree_iterparse        | 84.0 ms                                                                | 83.4 ms: 1.01x faster                                                         |
| docutils                   | 2.69 sec                                                               | 2.68 sec: 1.01x faster                                                        |
| coverage                   | 82.1 ms                                                                | 81.8 ms: 1.00x faster                                                         |
| spectral_norm              | 87.1 ms                                                                | 86.9 ms: 1.00x faster                                                         |
| bpe_tokeniser              | 4.02 sec                                                               | 4.01 sec: 1.00x faster                                                        |
| asyncio_websockets         | 544 ms                                                                 | 543 ms: 1.00x faster                                                          |
| fannkuch                   | 352 ms                                                                 | 354 ms: 1.00x slower                                                          |
| python_startup_no_site     | 7.35 ms                                                                | 7.38 ms: 1.01x slower                                                         |
| 2to3                       | 248 ms                                                                 | 250 ms: 1.01x slower                                                          |
| mako                       | 10.4 ms                                                                | 10.5 ms: 1.01x slower                                                         |
| python_startup             | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                         |
| shortest_path              | 425 ms                                                                 | 428 ms: 1.01x slower                                                          |
| scimark_fft                | 256 ms                                                                 | 259 ms: 1.01x slower                                                          |
| json_loads                 | 28.1 us                                                                | 28.5 us: 1.01x slower                                                         |
| richards                   | 17.7 ms                                                                | 17.9 ms: 1.01x slower                                                         |
| logging_silent             | 82.1 ns                                                                | 83.3 ns: 1.01x slower                                                         |
| sympy_expand               | 512 ms                                                                 | 519 ms: 1.01x slower                                                          |
| comprehensions             | 15.8 us                                                                | 16.0 us: 1.01x slower                                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 4.46 ms: 1.02x slower                                                         |
| meteor_contest             | 96.7 ms                                                                | 98.3 ms: 1.02x slower                                                         |
| scimark_sor                | 100 ms                                                                 | 103 ms: 1.02x slower                                                          |
| coroutines                 | 23.4 ms                                                                | 24.0 ms: 1.02x slower                                                         |
| many_optionals             | 976 us                                                                 | 999 us: 1.02x slower                                                          |
| json                       | 4.89 ms                                                                | 5.01 ms: 1.02x slower                                                         |
| create_gc_cycles           | 1.87 ms                                                                | 1.92 ms: 1.03x slower                                                         |
| pidigits                   | 192 ms                                                                 | 201 ms: 1.05x slower                                                          |
| regex_effbot               | 2.56 ms                                                                | 2.78 ms: 1.09x slower                                                         |
| regex_dna                  | 168 ms                                                                 | 183 ms: 1.09x slower                                                          |
| gc_traversal               | 4.07 ms                                                                | 4.47 ms: 1.10x slower                                                         |
| regex_v8                   | 21.2 ms                                                                | 24.0 ms: 1.13x slower                                                         |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (26): bench_mp_pool, async_tree_io, richards_super, pprint_safe_repr, float, sqlglot_v2_optimize, typing_runtime_protocols, async_tree_none, pickle_pure_python, dulwich_log, html5lib, sqlglot_v2_transpile, regex_compile, subparsers, generators, json_dumps, go, sympy_sum, sympy_integrate, pyflate, sphinx, sqlglot_v2_parse, sqlite_synth, scimark_lu, pylint, django_template

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 99.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x