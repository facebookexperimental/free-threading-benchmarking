# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: d47bed2
- commit date: 2025-11-06
- overall geometric mean: 1.062x faster
- HPT reliability: 96.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 251 ms: 1.02x faster                                                             |
| html5lib       | 61.4 ms                                                                | 69.5 ms: 1.13x slower                                                            |
| sphinx         | 993 ms                                                                 | 11.9 ms: 83.22x faster                                                           |
| Geometric mean | (ref)                                                                  | 4.21x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| coroutines                | 24.3 ms                                                                | 23.9 ms: 1.02x faster                                                            |
| async_generators          | 364 ms                                                                 | 368 ms: 1.01x slower                                                             |
| async_tree_memoization_tg | 306 ms                                                                 | 310 ms: 1.01x slower                                                             |
| async_tree_memoization    | 306 ms                                                                 | 315 ms: 1.03x slower                                                             |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (7): asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 70.6 ms                                                                | 60.6 ms: 1.17x faster                                                            |
| nbody          | 84.6 ms                                                                | 73.1 ms: 1.16x faster                                                            |
| pidigits       | 209 ms                                                                 | 192 ms: 1.09x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 180 ms: 1.03x slower                                                             |
| regex_effbot   | 2.59 ms                                                                | 2.94 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 307 us                                                                 | 298 us: 1.03x faster                                                             |
| json_dumps           | 9.31 ms                                                                | 9.11 ms: 1.02x faster                                                            |
| xml_etree_iterparse  | 85.4 ms                                                                | 84.0 ms: 1.02x faster                                                            |
| unpickle_pure_python | 184 us                                                                 | 185 us: 1.01x slower                                                             |
| json_loads           | 27.9 us                                                                | 28.2 us: 1.01x slower                                                            |
| tomli_loads          | 1.75 sec                                                               | 1.80 sec: 1.03x slower                                                           |
| xml_etree_process    | 53.7 ms                                                                | 55.5 ms: 1.03x slower                                                            |
| xml_etree_generate   | 77.0 ms                                                                | 80.9 ms: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                | 7.26 ms: 1.00x slower                                                            |
| python_startup         | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                            |
| django_template | 34.6 ms                                                                | 35.5 ms: 1.03x slower                                                            |
| genshi_text     | 20.5 ms                                                                | 21.5 ms: 1.05x slower                                                            |
| genshi_xml      | 49.3 ms                                                                | 56.0 ms: 1.14x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                                     |

All benchmarks:
===============

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-d47bed2 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| sphinx                    | 993 ms                                                                 | 11.9 ms: 83.22x faster                                                           |
| richards                  | 42.2 ms                                                                | 20.6 ms: 2.05x faster                                                            |
| richards_super            | 48.4 ms                                                                | 24.2 ms: 2.00x faster                                                            |
| float                     | 70.6 ms                                                                | 60.6 ms: 1.17x faster                                                            |
| logging_silent            | 99.6 ns                                                                | 85.8 ns: 1.16x faster                                                            |
| nbody                     | 84.6 ms                                                                | 73.1 ms: 1.16x faster                                                            |
| spectral_norm             | 96.7 ms                                                                | 86.0 ms: 1.13x faster                                                            |
| scimark_monte_carlo       | 62.0 ms                                                                | 55.2 ms: 1.12x faster                                                            |
| deltablue                 | 3.15 ms                                                                | 2.84 ms: 1.11x faster                                                            |
| scimark_sor               | 108 ms                                                                 | 98.7 ms: 1.09x faster                                                            |
| pidigits                  | 209 ms                                                                 | 192 ms: 1.09x faster                                                             |
| chaos                     | 57.1 ms                                                                | 52.9 ms: 1.08x faster                                                            |
| pyflate                   | 401 ms                                                                 | 380 ms: 1.06x faster                                                             |
| go                        | 107 ms                                                                 | 101 ms: 1.05x faster                                                             |
| scimark_lu                | 110 ms                                                                 | 104 ms: 1.05x faster                                                             |
| deepcopy_memo             | 26.6 us                                                                | 25.5 us: 1.04x faster                                                            |
| pickle_pure_python        | 307 us                                                                 | 298 us: 1.03x faster                                                             |
| json_dumps                | 9.31 ms                                                                | 9.11 ms: 1.02x faster                                                            |
| crypto_pyaes              | 67.8 ms                                                                | 66.3 ms: 1.02x faster                                                            |
| gc_traversal              | 4.40 ms                                                                | 4.31 ms: 1.02x faster                                                            |
| coroutines                | 24.3 ms                                                                | 23.9 ms: 1.02x faster                                                            |
| xml_etree_iterparse       | 85.4 ms                                                                | 84.0 ms: 1.02x faster                                                            |
| 2to3                      | 255 ms                                                                 | 251 ms: 1.02x faster                                                             |
| logging_format            | 6.65 us                                                                | 6.55 us: 1.02x faster                                                            |
| k_core                    | 1.87 sec                                                               | 1.85 sec: 1.01x faster                                                           |
| scimark_fft               | 257 ms                                                                 | 255 ms: 1.01x faster                                                             |
| create_gc_cycles          | 1.94 ms                                                                | 1.93 ms: 1.01x faster                                                            |
| bench_mp_pool             | 12.6 ms                                                                | 12.6 ms: 1.01x faster                                                            |
| python_startup_no_site    | 7.24 ms                                                                | 7.26 ms: 1.00x slower                                                            |
| python_startup            | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                            |
| fannkuch                  | 363 ms                                                                 | 364 ms: 1.00x slower                                                             |
| unpickle_pure_python      | 184 us                                                                 | 185 us: 1.01x slower                                                             |
| shortest_path             | 436 ms                                                                 | 439 ms: 1.01x slower                                                             |
| mako                      | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                            |
| sqlglot_v2_transpile      | 1.51 ms                                                                | 1.52 ms: 1.01x slower                                                            |
| connected_components      | 390 ms                                                                 | 393 ms: 1.01x slower                                                             |
| async_generators          | 364 ms                                                                 | 368 ms: 1.01x slower                                                             |
| subparsers                | 45.0 ms                                                                | 45.5 ms: 1.01x slower                                                            |
| json_loads                | 27.9 us                                                                | 28.2 us: 1.01x slower                                                            |
| async_tree_memoization_tg | 306 ms                                                                 | 310 ms: 1.01x slower                                                             |
| bench_thread_pool         | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                            |
| meteor_contest            | 99.8 ms                                                                | 101 ms: 1.02x slower                                                             |
| telco                     | 159 ms                                                                 | 162 ms: 1.02x slower                                                             |
| typing_runtime_protocols  | 156 us                                                                 | 159 us: 1.02x slower                                                             |
| pathlib                   | 17.5 ms                                                                | 17.8 ms: 1.02x slower                                                            |
| comprehensions            | 16.1 us                                                                | 16.4 us: 1.02x slower                                                            |
| logging_simple            | 5.77 us                                                                | 5.88 us: 1.02x slower                                                            |
| thrift                    | 764 us                                                                 | 785 us: 1.03x slower                                                             |
| django_template           | 34.6 ms                                                                | 35.5 ms: 1.03x slower                                                            |
| regex_dna                 | 175 ms                                                                 | 180 ms: 1.03x slower                                                             |
| sympy_expand              | 487 ms                                                                 | 502 ms: 1.03x slower                                                             |
| async_tree_memoization    | 306 ms                                                                 | 315 ms: 1.03x slower                                                             |
| tomli_loads               | 1.75 sec                                                               | 1.80 sec: 1.03x slower                                                           |
| xml_etree_process         | 53.7 ms                                                                | 55.5 ms: 1.03x slower                                                            |
| hexiom                    | 5.97 ms                                                                | 6.17 ms: 1.03x slower                                                            |
| bpe_tokeniser             | 3.96 sec                                                               | 4.11 sec: 1.04x slower                                                           |
| coverage                  | 82.3 ms                                                                | 86.0 ms: 1.05x slower                                                            |
| deepcopy                  | 245 us                                                                 | 256 us: 1.05x slower                                                             |
| many_optionals            | 1.23 ms                                                                | 1.29 ms: 1.05x slower                                                            |
| genshi_text               | 20.5 ms                                                                | 21.5 ms: 1.05x slower                                                            |
| sqlglot_v2_optimize       | 51.4 ms                                                                | 54.0 ms: 1.05x slower                                                            |
| sqlglot_v2_normalize      | 103 ms                                                                 | 108 ms: 1.05x slower                                                             |
| xml_etree_generate        | 77.0 ms                                                                | 80.9 ms: 1.05x slower                                                            |
| sympy_integrate           | 19.4 ms                                                                | 20.4 ms: 1.05x slower                                                            |
| sympy_sum                 | 158 ms                                                                 | 168 ms: 1.06x slower                                                             |
| nqueens                   | 81.5 ms                                                                | 86.7 ms: 1.06x slower                                                            |
| pylint                    | 293 ms                                                                 | 313 ms: 1.07x slower                                                             |
| sympy_str                 | 282 ms                                                                 | 305 ms: 1.08x slower                                                             |
| raytrace                  | 251 ms                                                                 | 272 ms: 1.08x slower                                                             |
| generators                | 27.5 ms                                                                | 29.9 ms: 1.09x slower                                                            |
| dulwich_log               | 69.7 ms                                                                | 76.2 ms: 1.09x slower                                                            |
| regex_effbot              | 2.59 ms                                                                | 2.94 ms: 1.13x slower                                                            |
| html5lib                  | 61.4 ms                                                                | 69.5 ms: 1.13x slower                                                            |
| genshi_xml                | 49.3 ms                                                                | 56.0 ms: 1.14x slower                                                            |
| mdp                       | 1.16 sec                                                               | 1.34 sec: 1.15x slower                                                           |
| Geometric mean            | (ref)                                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (17): pprint_pformat, sqlglot_v2_parse, regex_compile, xml_etree_parse, scimark_sparse_mat_mult, asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed_tg, json, deepcopy_reduce, async_tree_io_tg, regex_v8, async_tree_cpu_io_mixed, async_tree_io, async_tree_none_tg, pprint_safe_repr, sqlite_synth
Ignored benchmarks (2) of results/bm-20251101-3.15.0a1+-b155414-JIT/bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414.json: docutils, pycparser

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 96.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x