# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f8a764a
- commit date: 2025-11-12
- overall geometric mean: 1.007x faster
- HPT reliability: 97.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 250 ms: 1.02x faster                                                    |
| html5lib       | 61.4 ms                                                                | 69.1 ms: 1.13x slower                                                   |
| sphinx         | 993 ms                                                                 | 1.03 sec: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none           | 249 ms                                                                 | 244 ms: 1.02x faster                                                    |
| async_generators          | 364 ms                                                                 | 360 ms: 1.01x faster                                                    |
| async_tree_memoization_tg | 306 ms                                                                 | 308 ms: 1.01x slower                                                    |
| async_tree_io_tg          | 594 ms                                                                 | 598 ms: 1.01x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (7): coroutines, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 70.6 ms                                                                | 59.4 ms: 1.19x faster                                                   |
| pidigits       | 209 ms                                                                 | 192 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 22.3 ms: 1.01x faster                                                   |
| regex_compile  | 126 ms                                                                 | 128 ms: 1.01x slower                                                    |
| regex_dna      | 175 ms                                                                 | 177 ms: 1.01x slower                                                    |
| regex_effbot   | 2.59 ms                                                                | 2.77 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 307 us                                                                 | 295 us: 1.04x faster                                                    |
| xml_etree_iterparse  | 85.4 ms                                                                | 83.1 ms: 1.03x faster                                                   |
| unpickle_pure_python | 184 us                                                                 | 185 us: 1.01x slower                                                    |
| json_dumps           | 9.31 ms                                                                | 9.38 ms: 1.01x slower                                                   |
| xml_etree_generate   | 77.0 ms                                                                | 78.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 55.6 ms: 1.03x slower                                                   |
| tomli_loads          | 1.75 sec                                                               | 1.84 sec: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                | 7.26 ms: 1.00x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                   |
| django_template | 34.6 ms                                                                | 35.7 ms: 1.03x slower                                                   |
| genshi_text     | 20.5 ms                                                                | 21.8 ms: 1.06x slower                                                   |
| genshi_xml      | 49.3 ms                                                                | 55.4 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                  | 42.2 ms                                                                | 21.7 ms: 1.94x faster                                                   |
| richards_super            | 48.4 ms                                                                | 26.0 ms: 1.86x faster                                                   |
| float                     | 70.6 ms                                                                | 59.4 ms: 1.19x faster                                                   |
| spectral_norm             | 96.7 ms                                                                | 82.3 ms: 1.18x faster                                                   |
| logging_silent            | 99.6 ns                                                                | 86.5 ns: 1.15x faster                                                   |
| scimark_monte_carlo       | 62.0 ms                                                                | 55.3 ms: 1.12x faster                                                   |
| scimark_sor               | 108 ms                                                                 | 96.7 ms: 1.11x faster                                                   |
| pidigits                  | 209 ms                                                                 | 192 ms: 1.09x faster                                                    |
| scimark_lu                | 110 ms                                                                 | 101 ms: 1.08x faster                                                    |
| pyflate                   | 401 ms                                                                 | 376 ms: 1.07x faster                                                    |
| chaos                     | 57.1 ms                                                                | 54.3 ms: 1.05x faster                                                   |
| pickle_pure_python        | 307 us                                                                 | 295 us: 1.04x faster                                                    |
| thrift                    | 764 us                                                                 | 738 us: 1.04x faster                                                    |
| scimark_sparse_mat_mult   | 4.21 ms                                                                | 4.07 ms: 1.04x faster                                                   |
| go                        | 107 ms                                                                 | 103 ms: 1.03x faster                                                    |
| crypto_pyaes              | 67.8 ms                                                                | 65.7 ms: 1.03x faster                                                   |
| xml_etree_iterparse       | 85.4 ms                                                                | 83.1 ms: 1.03x faster                                                   |
| pprint_pformat            | 1.44 sec                                                               | 1.40 sec: 1.02x faster                                                  |
| logging_format            | 6.65 us                                                                | 6.50 us: 1.02x faster                                                   |
| create_gc_cycles          | 1.94 ms                                                                | 1.90 ms: 1.02x faster                                                   |
| 2to3                      | 255 ms                                                                 | 250 ms: 1.02x faster                                                    |
| mako                      | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                   |
| async_tree_none           | 249 ms                                                                 | 244 ms: 1.02x faster                                                    |
| deepcopy_memo             | 26.6 us                                                                | 26.2 us: 1.01x faster                                                   |
| json                      | 5.00 ms                                                                | 4.93 ms: 1.01x faster                                                   |
| async_generators          | 364 ms                                                                 | 360 ms: 1.01x faster                                                    |
| scimark_fft               | 257 ms                                                                 | 254 ms: 1.01x faster                                                    |
| regex_v8                  | 22.6 ms                                                                | 22.3 ms: 1.01x faster                                                   |
| python_startup_no_site    | 7.24 ms                                                                | 7.26 ms: 1.00x slower                                                   |
| python_startup            | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| async_tree_memoization_tg | 306 ms                                                                 | 308 ms: 1.01x slower                                                    |
| unpickle_pure_python      | 184 us                                                                 | 185 us: 1.01x slower                                                    |
| async_tree_io_tg          | 594 ms                                                                 | 598 ms: 1.01x slower                                                    |
| json_dumps                | 9.31 ms                                                                | 9.38 ms: 1.01x slower                                                   |
| sqlglot_v2_parse          | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                                   |
| pathlib                   | 17.5 ms                                                                | 17.7 ms: 1.01x slower                                                   |
| bench_thread_pool         | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| regex_compile             | 126 ms                                                                 | 128 ms: 1.01x slower                                                    |
| shortest_path             | 436 ms                                                                 | 442 ms: 1.01x slower                                                    |
| sqlite_synth              | 2.21 us                                                                | 2.24 us: 1.01x slower                                                   |
| regex_dna                 | 175 ms                                                                 | 177 ms: 1.01x slower                                                    |
| subparsers                | 45.0 ms                                                                | 45.7 ms: 1.02x slower                                                   |
| sqlglot_v2_transpile      | 1.51 ms                                                                | 1.53 ms: 1.02x slower                                                   |
| xml_etree_generate        | 77.0 ms                                                                | 78.9 ms: 1.03x slower                                                   |
| deepcopy                  | 245 us                                                                 | 251 us: 1.03x slower                                                    |
| connected_components      | 390 ms                                                                 | 400 ms: 1.03x slower                                                    |
| comprehensions            | 16.1 us                                                                | 16.6 us: 1.03x slower                                                   |
| django_template           | 34.6 ms                                                                | 35.7 ms: 1.03x slower                                                   |
| fannkuch                  | 363 ms                                                                 | 374 ms: 1.03x slower                                                    |
| hexiom                    | 5.97 ms                                                                | 6.17 ms: 1.03x slower                                                   |
| xml_etree_process         | 53.7 ms                                                                | 55.6 ms: 1.03x slower                                                   |
| gc_traversal              | 4.40 ms                                                                | 4.57 ms: 1.04x slower                                                   |
| sphinx                    | 993 ms                                                                 | 1.03 sec: 1.04x slower                                                  |
| bpe_tokeniser             | 3.96 sec                                                               | 4.14 sec: 1.05x slower                                                  |
| generators                | 27.5 ms                                                                | 28.7 ms: 1.05x slower                                                   |
| sqlglot_v2_normalize      | 103 ms                                                                 | 107 ms: 1.05x slower                                                    |
| many_optionals            | 1.23 ms                                                                | 1.29 ms: 1.05x slower                                                   |
| raytrace                  | 251 ms                                                                 | 264 ms: 1.05x slower                                                    |
| tomli_loads               | 1.75 sec                                                               | 1.84 sec: 1.05x slower                                                  |
| sqlglot_v2_optimize       | 51.4 ms                                                                | 54.3 ms: 1.06x slower                                                   |
| sympy_expand              | 487 ms                                                                 | 516 ms: 1.06x slower                                                    |
| pylint                    | 293 ms                                                                 | 311 ms: 1.06x slower                                                    |
| genshi_text               | 20.5 ms                                                                | 21.8 ms: 1.06x slower                                                   |
| nqueens                   | 81.5 ms                                                                | 87.0 ms: 1.07x slower                                                   |
| regex_effbot              | 2.59 ms                                                                | 2.77 ms: 1.07x slower                                                   |
| dulwich_log               | 69.7 ms                                                                | 75.5 ms: 1.08x slower                                                   |
| sympy_integrate           | 19.4 ms                                                                | 21.2 ms: 1.09x slower                                                   |
| sympy_sum                 | 158 ms                                                                 | 175 ms: 1.11x slower                                                    |
| sympy_str                 | 282 ms                                                                 | 316 ms: 1.12x slower                                                    |
| genshi_xml                | 49.3 ms                                                                | 55.4 ms: 1.12x slower                                                   |
| html5lib                  | 61.4 ms                                                                | 69.1 ms: 1.13x slower                                                   |
| deltablue                 | 3.15 ms                                                                | 3.63 ms: 1.15x slower                                                   |
| mdp                       | 1.16 sec                                                               | 1.34 sec: 1.15x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (20): nbody, meteor_contest, pprint_safe_repr, bench_mp_pool, coroutines, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, typing_runtime_protocols, coverage, asyncio_websockets, json_loads, logging_simple, pycparser, xml_etree_parse, k_core, async_tree_memoization, telco, deepcopy_reduce, async_tree_none_tg, async_tree_io
Ignored benchmarks (1) of results/bm-20251101-3.15.0a1+-b155414-JIT/bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414.json: docutils

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 97.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x