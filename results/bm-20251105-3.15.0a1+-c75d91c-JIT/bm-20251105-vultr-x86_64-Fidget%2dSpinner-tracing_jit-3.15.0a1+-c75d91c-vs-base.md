# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: c75d91c
- commit date: 2025-11-05
- overall geometric mean: 1.009x faster
- HPT reliability: 93.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 250 ms: 1.02x faster                                                    |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                  |
| html5lib       | 61.4 ms                                                                | 67.5 ms: 1.10x slower                                                   |
| sphinx         | 993 ms                                                                 | 1.03 sec: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                | 24.3 ms                                                                | 24.0 ms: 1.01x faster                                                   |
| async_tree_io_tg          | 594 ms                                                                 | 601 ms: 1.01x slower                                                    |
| async_tree_memoization_tg | 306 ms                                                                 | 311 ms: 1.01x slower                                                    |
| async_tree_memoization    | 306 ms                                                                 | 314 ms: 1.03x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (7): async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_io, async_generators, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 70.6 ms                                                                | 60.1 ms: 1.17x faster                                                   |
| pidigits       | 209 ms                                                                 | 201 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 21.6 ms: 1.05x faster                                                   |
| regex_dna      | 175 ms                                                                 | 171 ms: 1.02x faster                                                    |
| regex_effbot   | 2.59 ms                                                                | 2.57 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python  | 307 us                                                                 | 298 us: 1.03x faster                                                    |
| json_dumps          | 9.31 ms                                                                | 9.07 ms: 1.03x faster                                                   |
| xml_etree_iterparse | 85.4 ms                                                                | 84.7 ms: 1.01x faster                                                   |
| xml_etree_parse     | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| xml_etree_process   | 53.7 ms                                                                | 55.0 ms: 1.02x slower                                                   |
| xml_etree_generate  | 77.0 ms                                                                | 79.1 ms: 1.03x slower                                                   |
| tomli_loads         | 1.75 sec                                                               | 1.82 sec: 1.04x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                | 7.28 ms: 1.01x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                   |
| django_template | 34.6 ms                                                                | 35.9 ms: 1.04x slower                                                   |
| genshi_text     | 20.5 ms                                                                | 22.1 ms: 1.08x slower                                                   |
| genshi_xml      | 49.3 ms                                                                | 56.2 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                  | 42.2 ms                                                                | 21.4 ms: 1.97x faster                                                   |
| richards_super            | 48.4 ms                                                                | 25.6 ms: 1.89x faster                                                   |
| float                     | 70.6 ms                                                                | 60.1 ms: 1.17x faster                                                   |
| spectral_norm             | 96.7 ms                                                                | 82.9 ms: 1.17x faster                                                   |
| logging_silent            | 99.6 ns                                                                | 86.2 ns: 1.16x faster                                                   |
| scimark_monte_carlo       | 62.0 ms                                                                | 55.2 ms: 1.12x faster                                                   |
| deltablue                 | 3.15 ms                                                                | 2.81 ms: 1.12x faster                                                   |
| scimark_sor               | 108 ms                                                                 | 96.9 ms: 1.11x faster                                                   |
| pyflate                   | 401 ms                                                                 | 367 ms: 1.09x faster                                                    |
| chaos                     | 57.1 ms                                                                | 53.2 ms: 1.07x faster                                                   |
| deepcopy_memo             | 26.6 us                                                                | 25.3 us: 1.05x faster                                                   |
| regex_v8                  | 22.6 ms                                                                | 21.6 ms: 1.05x faster                                                   |
| scimark_lu                | 110 ms                                                                 | 105 ms: 1.04x faster                                                    |
| pidigits                  | 209 ms                                                                 | 201 ms: 1.04x faster                                                    |
| pprint_pformat            | 1.44 sec                                                               | 1.39 sec: 1.04x faster                                                  |
| go                        | 107 ms                                                                 | 103 ms: 1.03x faster                                                    |
| pickle_pure_python        | 307 us                                                                 | 298 us: 1.03x faster                                                    |
| json_dumps                | 9.31 ms                                                                | 9.07 ms: 1.03x faster                                                   |
| crypto_pyaes              | 67.8 ms                                                                | 66.1 ms: 1.02x faster                                                   |
| regex_dna                 | 175 ms                                                                 | 171 ms: 1.02x faster                                                    |
| scimark_fft               | 257 ms                                                                 | 252 ms: 1.02x faster                                                    |
| 2to3                      | 255 ms                                                                 | 250 ms: 1.02x faster                                                    |
| mako                      | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                   |
| json                      | 5.00 ms                                                                | 4.91 ms: 1.02x faster                                                   |
| coroutines                | 24.3 ms                                                                | 24.0 ms: 1.01x faster                                                   |
| sqlite_synth              | 2.21 us                                                                | 2.18 us: 1.01x faster                                                   |
| coverage                  | 82.3 ms                                                                | 81.5 ms: 1.01x faster                                                   |
| regex_effbot              | 2.59 ms                                                                | 2.57 ms: 1.01x faster                                                   |
| xml_etree_iterparse       | 85.4 ms                                                                | 84.7 ms: 1.01x faster                                                   |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| python_startup_no_site    | 7.24 ms                                                                | 7.28 ms: 1.01x slower                                                   |
| python_startup            | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| fannkuch                  | 363 ms                                                                 | 366 ms: 1.01x slower                                                    |
| meteor_contest            | 99.8 ms                                                                | 101 ms: 1.01x slower                                                    |
| bench_thread_pool         | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| async_tree_io_tg          | 594 ms                                                                 | 601 ms: 1.01x slower                                                    |
| sqlglot_v2_transpile      | 1.51 ms                                                                | 1.53 ms: 1.01x slower                                                   |
| shortest_path             | 436 ms                                                                 | 442 ms: 1.01x slower                                                    |
| async_tree_memoization_tg | 306 ms                                                                 | 311 ms: 1.01x slower                                                    |
| connected_components      | 390 ms                                                                 | 396 ms: 1.02x slower                                                    |
| telco                     | 159 ms                                                                 | 162 ms: 1.02x slower                                                    |
| typing_runtime_protocols  | 156 us                                                                 | 159 us: 1.02x slower                                                    |
| hexiom                    | 5.97 ms                                                                | 6.10 ms: 1.02x slower                                                   |
| subparsers                | 45.0 ms                                                                | 46.0 ms: 1.02x slower                                                   |
| xml_etree_process         | 53.7 ms                                                                | 55.0 ms: 1.02x slower                                                   |
| logging_simple            | 5.77 us                                                                | 5.93 us: 1.03x slower                                                   |
| xml_etree_generate        | 77.0 ms                                                                | 79.1 ms: 1.03x slower                                                   |
| async_tree_memoization    | 306 ms                                                                 | 314 ms: 1.03x slower                                                    |
| pathlib                   | 17.5 ms                                                                | 18.0 ms: 1.03x slower                                                   |
| sphinx                    | 993 ms                                                                 | 1.03 sec: 1.04x slower                                                  |
| deepcopy_reduce           | 2.59 us                                                                | 2.68 us: 1.04x slower                                                   |
| django_template           | 34.6 ms                                                                | 35.9 ms: 1.04x slower                                                   |
| deepcopy                  | 245 us                                                                 | 254 us: 1.04x slower                                                    |
| tomli_loads               | 1.75 sec                                                               | 1.82 sec: 1.04x slower                                                  |
| bpe_tokeniser             | 3.96 sec                                                               | 4.14 sec: 1.04x slower                                                  |
| sympy_expand              | 487 ms                                                                 | 510 ms: 1.05x slower                                                    |
| many_optionals            | 1.23 ms                                                                | 1.30 ms: 1.05x slower                                                   |
| docutils                  | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                  |
| sympy_integrate           | 19.4 ms                                                                | 20.5 ms: 1.06x slower                                                   |
| sqlglot_v2_optimize       | 51.4 ms                                                                | 54.4 ms: 1.06x slower                                                   |
| nqueens                   | 81.5 ms                                                                | 86.4 ms: 1.06x slower                                                   |
| generators                | 27.5 ms                                                                | 29.3 ms: 1.07x slower                                                   |
| sqlglot_v2_normalize      | 103 ms                                                                 | 109 ms: 1.07x slower                                                    |
| sympy_sum                 | 158 ms                                                                 | 169 ms: 1.07x slower                                                    |
| gc_traversal              | 4.40 ms                                                                | 4.72 ms: 1.07x slower                                                   |
| pylint                    | 293 ms                                                                 | 314 ms: 1.07x slower                                                    |
| genshi_text               | 20.5 ms                                                                | 22.1 ms: 1.08x slower                                                   |
| dulwich_log               | 69.7 ms                                                                | 75.3 ms: 1.08x slower                                                   |
| sympy_str                 | 282 ms                                                                 | 310 ms: 1.10x slower                                                    |
| html5lib                  | 61.4 ms                                                                | 67.5 ms: 1.10x slower                                                   |
| raytrace                  | 251 ms                                                                 | 276 ms: 1.10x slower                                                    |
| genshi_xml                | 49.3 ms                                                                | 56.2 ms: 1.14x slower                                                   |
| mdp                       | 1.16 sec                                                               | 1.36 sec: 1.17x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (21): pycparser, async_tree_none, async_tree_cpu_io_mixed_tg, pprint_safe_repr, create_gc_cycles, bench_mp_pool, async_tree_cpu_io_mixed, comprehensions, regex_compile, unpickle_pure_python, k_core, asyncio_websockets, json_loads, sqlglot_v2_parse, async_tree_io, async_generators, scimark_sparse_mat_mult, logging_format, thrift, async_tree_none_tg, nbody

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 93.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x