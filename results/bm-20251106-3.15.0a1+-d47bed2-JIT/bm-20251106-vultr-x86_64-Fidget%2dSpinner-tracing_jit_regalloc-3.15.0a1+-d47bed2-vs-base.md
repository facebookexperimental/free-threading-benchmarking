# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: d47bed2
- commit date: 2025-11-06
- overall geometric mean: 1.061x faster
- HPT reliability: 99.12%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 251 ms: 1.02x faster                                                             |
| html5lib       | 61.4 ms                                                                | 68.0 ms: 1.11x slower                                                            |
| sphinx         | 993 ms                                                                 | 11.9 ms: 83.38x faster                                                           |
| Geometric mean | (ref)                                                                  | 4.25x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| coroutines                | 24.3 ms                                                                | 23.9 ms: 1.02x faster                                                            |
| async_tree_cpu_io_mixed   | 484 ms                                                                 | 489 ms: 1.01x slower                                                             |
| async_tree_memoization_tg | 306 ms                                                                 | 311 ms: 1.02x slower                                                             |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (8): asyncio_websockets, async_generators, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 84.6 ms                                                                | 72.7 ms: 1.16x faster                                                            |
| float          | 70.6 ms                                                                | 61.6 ms: 1.15x faster                                                            |
| pidigits       | 209 ms                                                                 | 207 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 22.2 ms: 1.01x faster                                                            |
| regex_compile  | 126 ms                                                                 | 125 ms: 1.01x faster                                                             |
| regex_dna      | 175 ms                                                                 | 185 ms: 1.06x slower                                                             |
| regex_effbot   | 2.59 ms                                                                | 2.83 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 307 us                                                                 | 299 us: 1.03x faster                                                             |
| json_dumps           | 9.31 ms                                                                | 9.09 ms: 1.02x faster                                                            |
| xml_etree_iterparse  | 85.4 ms                                                                | 83.9 ms: 1.02x faster                                                            |
| xml_etree_parse      | 129 ms                                                                 | 129 ms: 1.00x faster                                                             |
| unpickle_pure_python | 184 us                                                                 | 185 us: 1.01x slower                                                             |
| json_loads           | 27.9 us                                                                | 28.1 us: 1.01x slower                                                            |
| tomli_loads          | 1.75 sec                                                               | 1.79 sec: 1.03x slower                                                           |
| xml_etree_process    | 53.7 ms                                                                | 55.4 ms: 1.03x slower                                                            |
| xml_etree_generate   | 77.0 ms                                                                | 80.8 ms: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                | 7.29 ms: 1.01x slower                                                            |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                            |
| django_template | 34.6 ms                                                                | 35.3 ms: 1.02x slower                                                            |
| genshi_text     | 20.5 ms                                                                | 21.6 ms: 1.05x slower                                                            |
| genshi_xml      | 49.3 ms                                                                | 55.0 ms: 1.12x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                                     |

All benchmarks:
===============

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| sphinx                    | 993 ms                                                                 | 11.9 ms: 83.38x faster                                                           |
| richards                  | 42.2 ms                                                                | 20.3 ms: 2.08x faster                                                            |
| richards_super            | 48.4 ms                                                                | 24.3 ms: 1.99x faster                                                            |
| nbody                     | 84.6 ms                                                                | 72.7 ms: 1.16x faster                                                            |
| float                     | 70.6 ms                                                                | 61.6 ms: 1.15x faster                                                            |
| logging_silent            | 99.6 ns                                                                | 88.1 ns: 1.13x faster                                                            |
| scimark_monte_carlo       | 62.0 ms                                                                | 55.0 ms: 1.13x faster                                                            |
| spectral_norm             | 96.7 ms                                                                | 87.8 ms: 1.10x faster                                                            |
| deltablue                 | 3.15 ms                                                                | 2.87 ms: 1.10x faster                                                            |
| scimark_sor               | 108 ms                                                                 | 98.2 ms: 1.10x faster                                                            |
| pyflate                   | 401 ms                                                                 | 378 ms: 1.06x faster                                                             |
| chaos                     | 57.1 ms                                                                | 53.7 ms: 1.06x faster                                                            |
| scimark_lu                | 110 ms                                                                 | 104 ms: 1.06x faster                                                             |
| go                        | 107 ms                                                                 | 101 ms: 1.05x faster                                                             |
| deepcopy_memo             | 26.6 us                                                                | 25.6 us: 1.04x faster                                                            |
| logging_format            | 6.65 us                                                                | 6.45 us: 1.03x faster                                                            |
| pickle_pure_python        | 307 us                                                                 | 299 us: 1.03x faster                                                             |
| json_dumps                | 9.31 ms                                                                | 9.09 ms: 1.02x faster                                                            |
| 2to3                      | 255 ms                                                                 | 251 ms: 1.02x faster                                                             |
| xml_etree_iterparse       | 85.4 ms                                                                | 83.9 ms: 1.02x faster                                                            |
| coroutines                | 24.3 ms                                                                | 23.9 ms: 1.02x faster                                                            |
| regex_v8                  | 22.6 ms                                                                | 22.2 ms: 1.01x faster                                                            |
| logging_simple            | 5.77 us                                                                | 5.71 us: 1.01x faster                                                            |
| scimark_fft               | 257 ms                                                                 | 254 ms: 1.01x faster                                                             |
| pidigits                  | 209 ms                                                                 | 207 ms: 1.01x faster                                                             |
| crypto_pyaes              | 67.8 ms                                                                | 67.3 ms: 1.01x faster                                                            |
| regex_compile             | 126 ms                                                                 | 125 ms: 1.01x faster                                                             |
| k_core                    | 1.87 sec                                                               | 1.86 sec: 1.01x faster                                                           |
| xml_etree_parse           | 129 ms                                                                 | 129 ms: 1.00x faster                                                             |
| bench_thread_pool         | 1.01 ms                                                                | 1.01 ms: 1.00x slower                                                            |
| python_startup_no_site    | 7.24 ms                                                                | 7.29 ms: 1.01x slower                                                            |
| python_startup            | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                            |
| mako                      | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                            |
| unpickle_pure_python      | 184 us                                                                 | 185 us: 1.01x slower                                                             |
| sqlglot_v2_transpile      | 1.51 ms                                                                | 1.52 ms: 1.01x slower                                                            |
| json_loads                | 27.9 us                                                                | 28.1 us: 1.01x slower                                                            |
| async_tree_cpu_io_mixed   | 484 ms                                                                 | 489 ms: 1.01x slower                                                             |
| meteor_contest            | 99.8 ms                                                                | 101 ms: 1.01x slower                                                             |
| fannkuch                  | 363 ms                                                                 | 367 ms: 1.01x slower                                                             |
| subparsers                | 45.0 ms                                                                | 45.6 ms: 1.01x slower                                                            |
| typing_runtime_protocols  | 156 us                                                                 | 159 us: 1.02x slower                                                             |
| deepcopy_reduce           | 2.59 us                                                                | 2.63 us: 1.02x slower                                                            |
| async_tree_memoization_tg | 306 ms                                                                 | 311 ms: 1.02x slower                                                             |
| telco                     | 159 ms                                                                 | 162 ms: 1.02x slower                                                             |
| django_template           | 34.6 ms                                                                | 35.3 ms: 1.02x slower                                                            |
| shortest_path             | 436 ms                                                                 | 446 ms: 1.02x slower                                                             |
| tomli_loads               | 1.75 sec                                                               | 1.79 sec: 1.03x slower                                                           |
| thrift                    | 764 us                                                                 | 784 us: 1.03x slower                                                             |
| bpe_tokeniser             | 3.96 sec                                                               | 4.07 sec: 1.03x slower                                                           |
| scimark_sparse_mat_mult   | 4.21 ms                                                                | 4.33 ms: 1.03x slower                                                            |
| xml_etree_process         | 53.7 ms                                                                | 55.4 ms: 1.03x slower                                                            |
| hexiom                    | 5.97 ms                                                                | 6.17 ms: 1.03x slower                                                            |
| gc_traversal              | 4.40 ms                                                                | 4.55 ms: 1.03x slower                                                            |
| connected_components      | 390 ms                                                                 | 403 ms: 1.04x slower                                                             |
| deepcopy                  | 245 us                                                                 | 254 us: 1.04x slower                                                             |
| many_optionals            | 1.23 ms                                                                | 1.28 ms: 1.04x slower                                                            |
| sympy_expand              | 487 ms                                                                 | 508 ms: 1.04x slower                                                             |
| xml_etree_generate        | 77.0 ms                                                                | 80.8 ms: 1.05x slower                                                            |
| sympy_integrate           | 19.4 ms                                                                | 20.4 ms: 1.05x slower                                                            |
| sqlglot_v2_normalize      | 103 ms                                                                 | 108 ms: 1.05x slower                                                             |
| genshi_text               | 20.5 ms                                                                | 21.6 ms: 1.05x slower                                                            |
| sqlglot_v2_optimize       | 51.4 ms                                                                | 54.2 ms: 1.05x slower                                                            |
| nqueens                   | 81.5 ms                                                                | 86.2 ms: 1.06x slower                                                            |
| regex_dna                 | 175 ms                                                                 | 185 ms: 1.06x slower                                                             |
| sympy_sum                 | 158 ms                                                                 | 169 ms: 1.07x slower                                                             |
| coverage                  | 82.3 ms                                                                | 87.9 ms: 1.07x slower                                                            |
| pylint                    | 293 ms                                                                 | 314 ms: 1.07x slower                                                             |
| dulwich_log               | 69.7 ms                                                                | 74.9 ms: 1.08x slower                                                            |
| generators                | 27.5 ms                                                                | 29.6 ms: 1.08x slower                                                            |
| raytrace                  | 251 ms                                                                 | 271 ms: 1.08x slower                                                             |
| sympy_str                 | 282 ms                                                                 | 306 ms: 1.08x slower                                                             |
| regex_effbot              | 2.59 ms                                                                | 2.83 ms: 1.09x slower                                                            |
| html5lib                  | 61.4 ms                                                                | 68.0 ms: 1.11x slower                                                            |
| genshi_xml                | 49.3 ms                                                                | 55.0 ms: 1.12x slower                                                            |
| mdp                       | 1.16 sec                                                               | 1.33 sec: 1.15x slower                                                           |
| Geometric mean            | (ref)                                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (17): sqlite_synth, comprehensions, asyncio_websockets, bench_mp_pool, sqlglot_v2_parse, async_generators, create_gc_cycles, async_tree_none, pprint_pformat, async_tree_io_tg, pathlib, json, async_tree_cpu_io_mixed_tg, async_tree_none_tg, pprint_safe_repr, async_tree_io, async_tree_memoization
Ignored benchmarks (2) of results/bm-20251101-3.15.0a1+-b155414-JIT/bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414.json: docutils, pycparser

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 99.12% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x