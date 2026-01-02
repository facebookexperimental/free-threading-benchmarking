# Results vs. base

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: linux-x86_64
- commit hash: b1e4adf
- commit date: 2026-01-01
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| docutils       | 2.69 sec                                                               | 2.68 sec: 1.01x faster                                                        |
| sphinx         | 998 ms                                                                 | 990 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 475 ms: 1.03x faster                                                          |
| async_tree_cpu_io_mixed    | 489 ms                                                                 | 476 ms: 1.03x faster                                                          |
| async_tree_none            | 243 ms                                                                 | 237 ms: 1.03x faster                                                          |
| async_tree_none_tg         | 243 ms                                                                 | 238 ms: 1.02x faster                                                          |
| async_tree_memoization_tg  | 306 ms                                                                 | 301 ms: 1.02x faster                                                          |
| async_tree_io_tg           | 588 ms                                                                 | 580 ms: 1.01x faster                                                          |
| async_generators           | 362 ms                                                                 | 359 ms: 1.01x faster                                                          |
| coroutines                 | 23.4 ms                                                                | 23.8 ms: 1.02x slower                                                         |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_io, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 75.3 ms                                                                | 73.9 ms: 1.02x faster                                                         |
| pidigits       | 192 ms                                                                 | 193 ms: 1.00x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 168 ms                                                                 | 167 ms: 1.01x faster                                                          |
| regex_compile  | 121 ms                                                                 | 120 ms: 1.01x faster                                                          |
| regex_v8       | 21.2 ms                                                                | 22.3 ms: 1.05x slower                                                         |
| regex_effbot   | 2.56 ms                                                                | 2.78 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps          | 9.51 ms                                                                | 9.36 ms: 1.02x faster                                                         |
| xml_etree_generate  | 78.6 ms                                                                | 77.4 ms: 1.02x faster                                                         |
| pickle_pure_python  | 278 us                                                                 | 275 us: 1.01x faster                                                          |
| json_loads          | 28.1 us                                                                | 27.9 us: 1.01x faster                                                         |
| xml_etree_parse     | 129 ms                                                                 | 129 ms: 1.01x faster                                                          |
| xml_etree_iterparse | 84.0 ms                                                                | 83.7 ms: 1.00x faster                                                         |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                | 12.5 ms: 1.00x slower                                                         |
| python_startup_no_site | 7.35 ms                                                                | 7.36 ms: 1.00x slower                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 52.1 ms                                                                | 49.3 ms: 1.06x faster                                                         |
| genshi_text    | 21.2 ms                                                                | 20.2 ms: 1.05x faster                                                         |
| mako           | 10.4 ms                                                                | 10.6 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml                 | 52.1 ms                                                                | 49.3 ms: 1.06x faster                                                         |
| genshi_text                | 21.2 ms                                                                | 20.2 ms: 1.05x faster                                                         |
| pprint_pformat             | 1.33 sec                                                               | 1.29 sec: 1.03x faster                                                        |
| nqueens                    | 86.8 ms                                                                | 84.4 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 475 ms: 1.03x faster                                                          |
| logging_format             | 6.76 us                                                                | 6.58 us: 1.03x faster                                                         |
| async_tree_cpu_io_mixed    | 489 ms                                                                 | 476 ms: 1.03x faster                                                          |
| async_tree_none            | 243 ms                                                                 | 237 ms: 1.03x faster                                                          |
| deepcopy                   | 244 us                                                                 | 238 us: 1.03x faster                                                          |
| pycparser                  | 1.11 sec                                                               | 1.09 sec: 1.03x faster                                                        |
| pprint_safe_repr           | 644 ms                                                                 | 628 ms: 1.02x faster                                                          |
| raytrace                   | 267 ms                                                                 | 261 ms: 1.02x faster                                                          |
| telco                      | 163 ms                                                                 | 159 ms: 1.02x faster                                                          |
| sympy_str                  | 309 ms                                                                 | 302 ms: 1.02x faster                                                          |
| async_tree_none_tg         | 243 ms                                                                 | 238 ms: 1.02x faster                                                          |
| pyflate                    | 364 ms                                                                 | 357 ms: 1.02x faster                                                          |
| richards_super             | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                         |
| dulwich_log                | 72.0 ms                                                                | 70.7 ms: 1.02x faster                                                         |
| scimark_monte_carlo        | 53.4 ms                                                                | 52.4 ms: 1.02x faster                                                         |
| nbody                      | 75.3 ms                                                                | 73.9 ms: 1.02x faster                                                         |
| sqlglot_v2_normalize       | 109 ms                                                                 | 107 ms: 1.02x faster                                                          |
| async_tree_memoization_tg  | 306 ms                                                                 | 301 ms: 1.02x faster                                                          |
| sqlglot_v2_optimize        | 54.2 ms                                                                | 53.3 ms: 1.02x faster                                                         |
| deepcopy_reduce            | 2.60 us                                                                | 2.56 us: 1.02x faster                                                         |
| coverage                   | 82.1 ms                                                                | 80.7 ms: 1.02x faster                                                         |
| json_dumps                 | 9.51 ms                                                                | 9.36 ms: 1.02x faster                                                         |
| mdp                        | 1.37 sec                                                               | 1.35 sec: 1.02x faster                                                        |
| hexiom                     | 6.09 ms                                                                | 6.00 ms: 1.02x faster                                                         |
| spectral_norm              | 87.1 ms                                                                | 85.8 ms: 1.02x faster                                                         |
| crypto_pyaes               | 67.0 ms                                                                | 66.0 ms: 1.02x faster                                                         |
| xml_etree_generate         | 78.6 ms                                                                | 77.4 ms: 1.02x faster                                                         |
| deltablue                  | 2.68 ms                                                                | 2.64 ms: 1.02x faster                                                         |
| async_tree_io_tg           | 588 ms                                                                 | 580 ms: 1.01x faster                                                          |
| sympy_sum                  | 169 ms                                                                 | 167 ms: 1.01x faster                                                          |
| deepcopy_memo              | 25.1 us                                                                | 24.8 us: 1.01x faster                                                         |
| k_core                     | 1.88 sec                                                               | 1.85 sec: 1.01x faster                                                        |
| pathlib                    | 17.7 ms                                                                | 17.5 ms: 1.01x faster                                                         |
| fannkuch                   | 352 ms                                                                 | 349 ms: 1.01x faster                                                          |
| pickle_pure_python         | 278 us                                                                 | 275 us: 1.01x faster                                                          |
| bench_thread_pool          | 1.31 ms                                                                | 1.30 ms: 1.01x faster                                                         |
| thrift                     | 734 us                                                                 | 727 us: 1.01x faster                                                          |
| regex_dna                  | 168 ms                                                                 | 167 ms: 1.01x faster                                                          |
| subparsers                 | 9.17 ms                                                                | 9.09 ms: 1.01x faster                                                         |
| connected_components       | 380 ms                                                                 | 377 ms: 1.01x faster                                                          |
| sphinx                     | 998 ms                                                                 | 990 ms: 1.01x faster                                                          |
| gc_traversal               | 4.07 ms                                                                | 4.04 ms: 1.01x faster                                                         |
| async_generators           | 362 ms                                                                 | 359 ms: 1.01x faster                                                          |
| regex_compile              | 121 ms                                                                 | 120 ms: 1.01x faster                                                          |
| sympy_integrate            | 20.2 ms                                                                | 20.1 ms: 1.01x faster                                                         |
| docutils                   | 2.69 sec                                                               | 2.68 sec: 1.01x faster                                                        |
| json_loads                 | 28.1 us                                                                | 27.9 us: 1.01x faster                                                         |
| xml_etree_parse            | 129 ms                                                                 | 129 ms: 1.01x faster                                                          |
| create_gc_cycles           | 1.87 ms                                                                | 1.86 ms: 1.00x faster                                                         |
| xml_etree_iterparse        | 84.0 ms                                                                | 83.7 ms: 1.00x faster                                                         |
| python_startup             | 12.5 ms                                                                | 12.5 ms: 1.00x slower                                                         |
| python_startup_no_site     | 7.35 ms                                                                | 7.36 ms: 1.00x slower                                                         |
| pidigits                   | 192 ms                                                                 | 193 ms: 1.00x slower                                                          |
| bpe_tokeniser              | 4.02 sec                                                               | 4.04 sec: 1.01x slower                                                        |
| typing_runtime_protocols   | 155 us                                                                 | 156 us: 1.01x slower                                                          |
| richards                   | 17.7 ms                                                                | 17.9 ms: 1.01x slower                                                         |
| generators                 | 28.9 ms                                                                | 29.3 ms: 1.01x slower                                                         |
| comprehensions             | 15.8 us                                                                | 16.0 us: 1.01x slower                                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 4.44 ms: 1.01x slower                                                         |
| many_optionals             | 976 us                                                                 | 989 us: 1.01x slower                                                          |
| scimark_fft                | 256 ms                                                                 | 260 ms: 1.01x slower                                                          |
| coroutines                 | 23.4 ms                                                                | 23.8 ms: 1.02x slower                                                         |
| meteor_contest             | 96.7 ms                                                                | 98.3 ms: 1.02x slower                                                         |
| mako                       | 10.4 ms                                                                | 10.6 ms: 1.02x slower                                                         |
| logging_silent             | 82.1 ns                                                                | 83.8 ns: 1.02x slower                                                         |
| regex_v8                   | 21.2 ms                                                                | 22.3 ms: 1.05x slower                                                         |
| regex_effbot               | 2.56 ms                                                                | 2.78 ms: 1.08x slower                                                         |
| bench_mp_pool              | 223 ms                                                                 | 258 ms: 1.16x slower                                                          |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (22): async_tree_memoization, logging_simple, sympy_expand, go, pylint, sqlglot_v2_transpile, async_tree_io, float, unpickle_pure_python, scimark_lu, html5lib, shortest_path, asyncio_websockets, xml_etree_process, 2to3, django_template, tomli_loads, chaos, json, sqlglot_v2_parse, sqlite_synth, scimark_sor

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x